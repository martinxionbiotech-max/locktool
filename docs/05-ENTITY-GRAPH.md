# 05 — Entity Graph (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义全站核心实体（Entity）、别名、层级关系、Canonical URL、Schema @id 与产品/来源映射。
> 状态：DRAFT v0.1
> 目标：让 Google 把 Locktool 理解为一个完整的 Locksmith knowledge entity；让 AI 能稳定抽取、引用、关联。

---

## 0. 为什么需要 Entity Graph

方案第 9/18 节核心思想：SEO 的下一层是**实体**，不是关键词。稳定、一致、可解析的实体图是 GEO/AIO 可引用性的地基。

**统一 @id 前缀**：`https://locktool.com/entity/{slug}#entity`（所有 Hub 共享同一 @id 命名空间，即使用子域，也指向主域 @id）。

---

## 1. 核心实体清单

### 组织与主体层
| Entity | @id | Canonical URL | 别名 | Parent |
|---|---|---|---|---|
| Locktool (Organization) | `#org` | `https://locktool.com/` | Locktool, Locktool.com | — |
| Locktool Knowledge Ecosystem | `#ecosystem` | `https://locktool.com/knowledge/` | — | Organization |
| Locktool Training Division | `#training` | `https://locktool.com/training/`（或 training.locktool.com） | — | Organization |

### 人物实体（E-E-A-T 根，必须真实，禁止虚构）
| Entity | @id | 角色 | 来源 |
|---|---|---|---|
| （待定：创始人/技术负责人） | `#person-founder` | 公司实体负责人 | 待用户提供真实信息 |
| （待定：主编/行业专家） | `#person-editor` | 内容审阅者 | 待用户提供真实资质 |

> 阻塞项：人物实体必须真实。在用户提供真实可挂靠的作者/专家前，此层标记 `[PENDING]`，不得虚构。

### 行业概念实体（High-level Domain Entites）
| Entity | @id | Definition（一句话） | Parent |
|---|---|---|---|
| Locksmith | `#locksmith` | 提供锁具安装、维修、钥匙服务与安防解决方案的专业人员 | — |
| Lock | `#lock` | 通过机械或电子机制控制开启的安防装置 | — |
| Cylinder | `#cylinder` | 锁的旋转核心组件，含 plug 与 housing | Lock |
| Key | `#key` | 使锁解锁的特制工具/凭证 | Lock |
| Key Blank | `#key-blank` | 未经切割的钥匙毛坯 | Key |
| Key Cutting | `#key-cutting` | 将钥匙毛坯切割为匹配锁的组合的过程 | Key |
| Locksmith Tool | `#locksmith-tool` | 锁匠专业使用的工具 | — |
| Automotive Locksmith | `#automotive-locksmith` | 专注于车辆锁具与钥匙系统的锁匠 | Locksmith |
| Security Technician | `#security-technician` | 从事安防系统安装维护的专业人员 | Locksmith |
| Training | `#training` | 锁匠专业教育与技能培养 | — |
| Certification | `#certification` | 行业资质认证（如 ALOA） | Training |
| Standard | `#standard` | 行业/安全标准（如 NFPA 80） | — |
| Manufacturer | `#manufacturer` | 锁匠工具制造实体 | — |
| Product Category | `#product-category` | 工具商品分类 | — |

---

## 2. 锁型实体层（Lock Type Entities）

| Entity | @id | Parent | 关键属性 |
|---|---|---|---|
| Pin Tumbler Lock | `#pin-tumbler` | Lock | key combinations ~100k（5-pin） |
| Wafer Lock | `#wafer` | Lock | 低安全，汽车/柜体常见 |
| Dimple Lock | `#dimple` | Lock | — |
| Tubular Lock | `#tubular` | Lock | 自动售货机/ATM |
| Disc Detainer Lock | `#disc-detainer` | Lock | Abloy Protec2 高安全 |
| Lever Lock | `#lever` | Lock | — |
| Padlock | `#padlock` | Lock | — |
| Smart Lock | `#smart-lock` | Lock | 电子/凭证 |

---

## 3. 工具实体层（Locksmith Tool Entities）

| Entity | @id | Parent | Risk Grade（见 01） |
|---|---|---|---|
| Lock Pick | `#lock-pick` | Locksmith Tool | B |
| Tension Tool / Wrench | `#tension-tool` | Locksmith Tool | B |
| Decoding Tool | `#decoding-tool` | Locksmith Tool | B |
| Key Cutting Machine | `#key-cutting-machine` | Locksmith Tool | A |
| Key Blank | `#key-blank` | Locksmith Tool | A |
| Impressioning Tool | `#impressioning-tool` | Locksmith Tool | A/B |
| Automotive Key Programmer | `#key-programmer` | Locksmith Tool | C |
| Immobilizer Tool | `#immobilizer-tool` | Locksmith Tool | C |
| Broken Key Extractor | `#key-extractor` | Locksmith Tool | A |
| Inspection / Measurement Tool | `#inspection-tool` | Locksmith Tool | A |

> 风险分级映射到 01 文档，C 类实体在公开内容中只做合规定位 + Responsible Use 提示，不做绕过教学。

---

## 4. 实体关系（关键三元组）

```
Locksmith → uses → Locksmith Tool
Locksmith → services → Lock
Lock → has-mechanism → {Pin Tumbler, Wafer, Disc Detainer, ...}
Lock → operated-by → Key
Key → derived-from → Key Blank
Key Cutting → produces → Key
Automotive Locksmith → programs → Transponder Key
Training → leads-to → Certification
Certification → governed-by → Standard
Product Category → contains → Locksmith Tool
Manufacturer → produces → Locksmith Tool
```

---

## 5. 每个实体的必填字段（Entity Template）

方案第 9 节要求每个实体至少含：
- Canonical URL
- Definition
- Aliases
- Related Entities
- Parent Entity
- Child Entities
- Products（关联 SKU）
- Sources（权威来源）

落地时每个实体一个"实体页"（若值得独立 URL），并在 Schema 中用 `sameAs` / `@id` / `isPartOf` 关联。

---

## 6. Schema 映射（实体 → 结构化数据）

| 实体类型 | Schema 类型 |
|---|---|
| Organization / 人物 | `Organization` / `Person` |
| 术语概念 | `DefinedTerm`（组织在 `DefinedTermSet`） |
| 锁型/工具分类 | `DefinedTerm` + `Thing` 关系 |
| 产品/分类 | `Product` / `ItemList` |
| 文章/指南 | `Article` / `TechArticle` |

> 关键：所有实体用统一 `@id`，跨 Hub / 子域一致引用，形成稳定 Entity Graph（方案 18 节）。

---

## 7. 待确认决策

1. **人物实体**：创始人与编辑的真实姓名/资质（E-E-A-T 必需，禁止虚构）。
2. **Manufacturer 实体**：Locktool 自有品牌？还是代理某中国锁匠工具厂商？这决定 Manufacturer 实体的定义与来源。

> 下一步：06-TOPIC-CLUSTERS.md、07-KEYWORD-MAP.md（把实体落到主题簇与关键词地图）。
