# 03 — Main Site Architecture (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义商业主站的信息架构（IA）、URL 结构、页面类型与职责。
> 状态：DRAFT v0.1
> 前提约束：见 01-LEGAL-RISK-MATRIX.md（产品四分级、合规定位、禁止语汇）。主站只承载 COMMERCIAL INTENT，informational/technical/educational 意图下沉到 Knowledge Hub。

---

## 0. 定位与职责

主站 = **Money Site**，唯一允许出现强商业意图与交易入口的地方。

- 解决商业意图：What is it? / Who is it for? / Why use it? / How is it different? / Specs / Compatibility / Professional application / Safety / Compliance / Shipping / Support
- 所有 informational 内容（原理、术语、对比、培训）**不在主站堆**，导向 Knowledge Hub / Technical Hub / Training Hub。

---

## 1. 信息架构（IA）

```
Locktool.com (主站)
├── /                       Home（品牌 + 价值主张 + 生态入口）
├── /products/              产品（按 SKU/型号）
├── /categories/            产品分类（A/B 类，见风险矩阵）
├── /applications/          应用场景（专业用途导向）
├── /industries/            行业（住宅/商业/汽车/机构）
├── /solutions/             专业解决方案（Solution 聚合页）
├── /resources/             资源（指向各 Knowledge Hub 的桥接入口）
├── /compliance/            合规中心（含 Responsible Use）
├── /manufacturing/         制造与质量（E-E-A-T 工厂/工艺背书）
├── /about/                 公司（实体信息 + 团队）
├── /contact/               联系 / 询价
└── /shipping-returns/      物流与退换（含法域限制说明）
```

> 注意：不是传统 Home/Products/Blog/About/Contact 五件套。新增 Applications / Industries / Solutions / Compliance / Manufacturing 维度，是为了在 YMYL + 双用途风险品类里建立更强的 E-E-A-T 与合规定位。

---

## 2. 页面类型与职责

### 2.1 Home（/）
- 一句话价值主张：**Professional Locksmith Tools & Lock Technology Resources**
- 强调 licensed/authorized/professional 定位
- 生态入口：主站 + Knowledge Hub + Technical Hub + Training Hub 的导航桥
- 禁止：任何"破解/偷窃"导向的 hero 文案

### 2.2 产品分类页（/categories/）
- 严格按 01 文档的风险分级组织：
  - **A 类**（key cutting accessories / hand tools / inspection / measuring / lock maintenance / training materials）
  - **B 类**（lock picks / tension tools / decoding tools / automotive locksmith equipment）→ 需受众区隔 + 合规定位文案
  - **C 类**（vehicle security bypass / immobilizer defeat / covert entry）→ 默认不展示公开价格，仅 "Contact a specialist"，且页面加 Responsible Use 提示 + 人工审核
  - **D 类** → 不建页面

### 2.3 应用场景页（/applications/）
- professional use / authorized use / lawful use / security training / lock technology education 导向
- 每个场景页回答：What / Who / Why / How different / 安全 / 合规 / 物流

### 2.4 行业页（/industries/）
- Residential / Commercial / Automotive / Institutional（机构）
- 汽车行业页必须强调 authorized automotive locksmith / dealer / security technician 定位，规避绕过式语言

### 2.5 专业解决方案页（/solutions/）
- 面向具体工作流（如 "rekeying 完整方案"、"汽车钥匙诊断与维修方案"）
- 承担 commercial funnel 的中间层（Knowledge → Solution → Product → Quote）

### 2.6 合规中心（/compliance/）
- Responsible Use Policy
- Jurisdiction / Import / Possession 限制说明（引用 01 文档，标注来源 + 日期 + 法域）
- 禁止过度堆免责声明

### 2.7 制造与质量页（/manufacturing/）
- 工厂、工艺、材质（spring steel / stainless / alloy）、QC、认证（ISO 等，须真实）
- E-E-A-T 关键页，作者/公司信息必须真实，禁止虚构

---

## 3. URL 架构

- 主站根域：`locktool.com`
- 层级用目录（非参数 URL）：
  - `/categories/{category-slug}/`
  - `/products/{product-slug}/`
  - `/applications/{application-slug}/`
- 短路规则：绝不用 `/blog/` 承载 informational 内容（那是 Knowledge Hub 的职责）。

---

## 4. 商业 funnel（主站视角）

```
Informational Query（Knowledge Hub 承接）
        ↓
Related Entity / Tool Selection Guide（Knowledge/Training Hub）
        ↓
Solution 页（主站 /solutions/）
        ↓
Product Category（/categories/）
        ↓
Product（/products/）
        ↓
Contact / Quote
```

主站只出现在 funnel 的后半段，天然承接已经建立了信任的高意图流量。

---

## 5. 结构数据（主站）

按页面类型部署（详见 09-SCHEMA，此处先规划）：
- Organization / WebSite / WebPage / BreadcrumbList / Product / ItemList
- Product schema 的价格字段：**若为询价模式，不填 lowPrice/highPrice**（避免 invalid），用 `offerCount` + `availability`（历史教训已记录在项目记忆中）

---

## 6. 待确认决策（阻塞项）

1. **主站域名最终定名**：`locktool.com` 是占位。需确认实际可用域名。
2. **目标首发市场**：US 优先？还是 US + UK + EU 同步？这决定 Jurisdiction 页面与物流页的信息颗粒度。
3. **产品线起点**：首批 SKU 是偏 A 类（安全稳妥快速起量）还是 B 类（核心利润但需合规打磨）？
4. **公司实体**：用哪个真实工商实体 + 可挂靠的作者/专家（E-E-A-T 根，禁止虚构）。

> 这四项会影响 03/04 的最终落地细节，但不阻塞 Knowledge Hub 架构（04）的骨架设计。
