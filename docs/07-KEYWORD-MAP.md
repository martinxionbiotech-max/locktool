# 07 — Keyword Map (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。把主题簇（06）映射到真实关键词、搜索意图与商业/内容属性。
> 状态：DRAFT v0.1
> 原则：不追求关键词数量，追求 Search Intent → 主题 → 实体 → 商业价值的对齐。所有关键词必须能落到具体页面 + 原创价值层。

---

## 0. 方法论

每个关键词维度：
- **Intent**：informational / commercial / transactional / navigational / comparison / entity
- **Entity**：挂靠的实体（05 文档）
- **Page Type**：Pillar / Cluster / Supporting / Entity / Commercial
- **Risk**：是否触及安全红线（01 文档）
- **Original Value Layer**：该页必须提供的原创价值（07 文档 §7）

---

## 1. 关键词 → 意图 → 页面映射表

> 注：以下为**初步关键词库（未做具体搜索量的精确核实，需后续用关键词工具校验量级）**。标注（量级待核）。

### 簇 1 — Locksmith Tools（商业意图为主）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| locksmith tools | commercial | #locksmith-tool | Commercial cat | A/B | 分类学导航 |
| professional locksmith tool kit | commercial | #locksmith-tool | Commercial | B | 专业 vs 初学套装矩阵 |
| lock pick set | commercial | #lock-pick | Commercial cat | **B** | 合规定位 + 选型 |
| lock pick set selection guide | commercial+info | #lock-pick | Cluster | B | 选型决策树 |
| tension wrench guide | informational | #tension-tool | Cluster | B | BOK vs TOK 量化对比 |
| hook pick vs rake | comparison | #lock-pick | Cluster | B | 场景/锁型适配表 |
| lock pick set legality / laws | informational | #locksmith-tool | Entity/Compliance | B | 法域矩阵（原创） |
| broken key extractor | commercial | #key-extractor | Commercial | A | 选型 + 使用 |

### 簇 2 — Lock Types（informational 为主）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| types of locks | informational | #lock | Pillar | A | 全锁型工程参数对比表 |
| pin tumbler lock how it works | informational | #pin-tumbler | Cluster | A | 机制图解 + 组合数计算 |
| wafer vs pin tumbler | comparison | #wafer #pin-tumbler | Cluster | A | 参数对比矩阵 |
| disc detainer lock | informational | #disc-detainer | Cluster | A | 高安全原理科普 |
| tubular lock | informational | #tubular | Cluster | A | 原理 + 应用 |

### 簇 3 — Key Systems（informational + technical）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| key blank types | informational | #key-blank | Cluster | A | 分类 + 兼容表 |
| key cutting machine | commercial | #key-cutting-machine | Commercial | A | 选型 + 场景 |
| master key system | informational | #key | Cluster | A | 原理 + 规划 |
| transponder key / chip key | informational | #key | Cluster | B/C | 原理科普（合规定位） |
| restricted key system | informational | #key | Cluster | A | 安全机制 |

### 簇 4 — Automotive Locksmith（technical，高风险隔离）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| automotive locksmith tools | commercial | #automotive-locksmith | Commercial | B/C | 分类导航 + 合规提示 |
| key programmer / key programming tool | commercial | #key-programmer | Commercial | **C** | 选型 + 技能门槛 + 合规 |
| car key programming how it works | informational | #key-programmer | Cluster | C | 原理解释（非绕过） |
| immobilizer system explained | informational | #immobilizer-tool | Cluster | C | 安全演进科普 |
| OEM vs aftermarket key | comparison | #key | Cluster | B | 对比表 |

> ⚠️ 簇 4 全部 C 类，任何"绕过防盗/免钥匙偷车"类关键词**一律排除**，不做。

### 簇 5 — Training / Certification（educational，E-E-A-T 杠杆）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| how to become a locksmith | informational | #training | Pillar | A | 分州/分步决策树 |
| locksmith certification | informational | #certification | Pillar | A | ALOA 16 认证全景图 |
| ALOA certification levels | informational | #certification | Cluster | A | 层级递进表 |
| locksmith license by state | informational | #certification | Cluster | A | 州法矩阵（原创） |
| locksmith training programs | informational | #training | Cluster | A | 路径对比 |
| locksmith apprenticeship | informational | #training | Cluster | A | 流程 + 州要求 |

### 簇 6 — Compliance（informational，安全红线优先）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| are lock picks legal | informational | #locksmith-tool | Entity/Compliance | B | 法域矩阵（来源+日期） |
| lock pick laws by state | informational | #locksmith-tool | Cluster | B | 州法全表（toool 对齐） |
| locksmith import restrictions | informational | #standard | Cluster | B | Jurisdiction Matrix |
| responsible use of locksmith tools | informational | #locksmith-tool | Compliance | A/B | 安全边界说明 |

### 簇 7 — Glossary（entity intent）

| 关键词 | Intent | Entity | Page Type | Risk | Original Value |
|---|---|---|---|---|---|
| locksmith terminology / glossary | entity | #glossary | Pillar | A | DefinedTermSet + @id |
| what is a [term]（spool pin / shear line / bitting...） | entity | 各术语实体 | Entity | A | DefinedTerm + 字段全 |

---

## 2. 关键词层级 → 内容层级

```
商业大词（locksmith tools）→ Commercial 分类页（克制，不堆词）
    ↑
Pillar（types of locks / certification）→ 高价值信息页
    ↑
Cluster / Supporting（长尾）→ 具体问题页 + 内容页
    ↑
Entity / Glossary → 实体页（AI 引用 + 内链枢纽）
```

---

## 3. 重点领域（Blue Ocean 对齐 02 文档）

| Blue Ocean | 对应关键词群 | Page Type |
|---|---|---|
| 合规/认证/法规图谱 | locksmith license by state / certification / lock pick laws | Pillar + Cluster + Compliance |
| 工具 Taxonomy | locksmith tool categories / tool classification | Pillar + Cluster |
| 深度对比 | wafer vs pin tumbler / BOK vs TOK / steel vs stainless | Cluster（对比模板） |
| 实体术语 | glossary + what is [term] | Entity（DefinedTerm） |

---

## 4. 待确认 / 阻塞项

1. **关键词量级需核实**：本表未做搜索量精确核实，需后续用关键词工具（如 Ahrefs/Google Keyword Planner/手动）补充量级与竞争度。
2. **商业 vs 内容配比**：主站商业页与 Knowledge Hub 信息页的数量配比，待 03/04 定稿后按 funnel 反推。
3. **首发市场语言**：US-only 还是多市场，影响关键词的地域前缀（如 "by state" 明确 US 导向）。

> 下一步：08-INTERNAL-LINKING-MAP.md、09-CONTENT-TEMPLATES.md。
