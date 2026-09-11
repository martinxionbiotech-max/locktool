# 01 — Legal & Safety Risk Matrix (Locksmith Tools)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义全站产品/内容/营销的法律与安全边界。
> 状态：DRAFT v0.1
> ⚠️ 本文件不是法律意见，不替代执业律师/各国官方监管机构的判断。凡标注 [UNKNOWN] 或 [REVIEW_REQUIRED] 的项，必须由具备相应司法辖区资质的法律专业人士复核后方可发布。

---

## 0. 绝对优先级（不可违背）

```
LEGAL / SAFETY
  >
SEARCH ENGINE COMPLIANCE
  >
TRUST / E-E-A-T
  >
INFORMATION QUALITY
  >
SEO
  >
AIO / GEO
  >
COMMERCIAL CONVERSION
```

任何产品、关键词、页面、内容或营销方式，只要触碰法律/安全红线，一律 **STOP**，标记 `[RISK]` / `[REVIEW_REQUIRED]`，说明风险原因、涉及国家/地区、风险等级与建议处理方式，不得自动发布。

---

## 1. 禁止定位（红线清单）

网站**不得**被定位为以下任何一类：

- burglary tools（入室盗窃工具）
- theft tools（盗窃工具）
- vehicle theft tools（偷车工具）
- bypass security tools（绕过安防工具）
- illegal entry tools（非法进入工具）
- anti-theft defeat tools（反防盗破解工具）
- tools for stealing vehicles（盗车工具）
- tools for unauthorized access（未授权访问工具）

**禁止使用的营销语言**（文案红线，含 title / meta / 正文 / 图片 alt / schema）：

- "open any car" / "unlock any vehicle"
- "steal a car"
- "bypass immobilizer" / "defeat security"
- "break into"
- "without key"
- "undetectable entry"

> 上述措辞一旦出现，直接拒绝发布，回退给人工审核。

---

## 2. 合规定位（正向表述）

全站统一定位为：

> **Professional Locksmith Tools & Lock Technology Resources**

核心受众与语汇：

- licensed locksmiths（持证锁匠）
- locksmith professionals / security technicians
- automotive locksmith professionals
- lock technicians / authorized security professionals
- training / diagnostics / maintenance / repair
- lock technology / security education / lawful access

**正向核心表达**（替代危险语汇）：

- "professional use" / "authorized use" / "lawful use"
- "security training" / "lock technology education"

> 注意：不要过度重复免责声明造成垃圾页面（disclaimer stuffing 本身也会被 Google 视为低质信号）。免责声明应集中、克制、出现在需要的页面（如合规页、高风险产品页、工具选择页）。

---

## 3. Product Risk Matrix（产品风险分级）

| 等级 | 定义 | 典型产品示例 | 处理方式 |
|---|---|---|---|
| **A — Low** | 通用、无单一用途滥用价值 | key cutting accessories、通用手工具、检视/量测器材、锁具维护用品、培训教材 | 正常纳入商业体系 |
| **B — Medium** | 专业用途工具，具一定双用途性 | lock picks、tension tools、decoding 相关工具、专业汽车锁匠设备 | 允许，但需合规定位 + 受众区隔 + 脱敏文案 |
| **C — High** | 涉及安防绕过/高度专用 | vehicle security bypass、immobilizer/security defeat、covert entry、高度专用 bypass 设备、潜在双用途安防工具 | **必须人工审核**，默认不自动发布 |
| **D — Restricted / Do Not Promote** | 明显面向盗窃/非法进入/规避 | 明确用于盗窃、未授权进入、规避安防、以非法为目的击败安防的产品/内容 | **不进商业营销体系** |

> C 类每一件产品/每一个页面都要单独建 review checklist；D 类彻底排除。

---

## 4. Jurisdiction Matrix（法域矩阵）

> 核心原则：**中国可生产 ≠ 全球可销售**。以下为初步框架，须逐项填充并经专业复核。

| Country/Region | Product | Legal Status | Import Restriction | Possession Restriction | Marketing Restriction | Platform Risk | Risk Level | Source | Last Checked |
|---|---|---|---|---|---|---|---|---|---|
| US | lock picks / pick sets | [REVIEW_REQUIRED] 州州不一（多数州"意图"导向合法，TN/MS/NV/OH 等需谨慎） | [UNKNOWN] | 多数州需"合法意图"，部分州 possession 为 prima facie 证据 | 禁止面向盗窃/未授权进入的表述 | 中 | B/C | toool.us, Wikipedia (lock_picking) | 2026-09-11 |
| UK (England & Wales) | lock picks / burglary tools | [REVIEW_REQUIRED] "going equipped / likely to be used in burglary" 罪名，最高 3 年（Crown） | [UNKNOWN] | 需"合法目的"抗辩；无正当理由持有可诉 | 禁止 burglary 导向 | 中高 | B/C | Wikipedia, UK theft act | 2026-09-11 |
| UK (Scotland) | lock picks | [UNKNOWN] | [UNKNOWN] | [UNKNOWN] | [UNKNOWN] | 中高 | [UNKNOWN] | 待补 | — |
| EU (general) | lock picks | 大多数成员国不监管持有 | 低 | 低（Hungary 例外，公共场所持有禁止） | 一般 | 低-中 | B | Wikipedia | 2026-09-11 |
| DE | lock picks | 合法（需物主许可） | 低 | 低 | 一般 | 低 | A/B | Wikipedia | 2026-09-11 |
| HU | lock picks | **公共场所持有禁止（特例）** | [UNKNOWN] | 高 | 高 | 高 | C/D | Wikipedia | 2026-09-11 |
| Canada | lock picks | [REVIEW_REQUIRED] 各省不一 | [UNKNOWN] | 部分省需 license | [UNKNOWN] | 中 | B/C | 待补 | — |
| AU | lock picks | [REVIEW_REQUIRED] 各州/领地不一 | [UNKNOWN] | 意图导向 | [UNKNOWN] | 中 | B/C | 待补 | — |
| NZ | lock picks | 合法，但持有用于犯罪意图最高 3 年 | [UNKNOWN] | 意图导向 | 一般 | 中 | B | lockpickings | 2026-09-11 |
| automotive key programming / immobilizer tools | [REVIEW_REQUIRED] 高风险：与车辆防盗绕过强相关 | [UNKNOWN] | [UNKNOWN] | 禁止"绕过防盗/免钥匙偷车" | 高 | **C** | 待补 | — |

> 说明：凡 [UNKNOWN] 或 [REVIEW_REQUIRED] 项，禁止 Agent 编造结论；必须引用官方政府、海关、监管机构或权威法律来源后填入。

---

## 5. Content Safety Boundary（内容安全边界）

Knowledge Hub 可以解释（WHITE）：

- **WHAT**（是什么）— 概念、术语、工具定义
- **WHY**（为什么）— 原理、设计逻辑
- **WHEN**（何时）— 适用场景、维护时机
- **HOW TO CHOOSE**（如何选择）— 选型、对比
- **HOW TO MAINTAIN**（如何维护）— 保养、存储
- **HOW TO TRAIN**（如何训练）— 培训、认证
- **HOW LOCK TECHNOLOGY WORKS**（锁具技术原理）

**禁止提供**（RED，特别是具滥用价值的内容）：

- 绕过具体车型防盗系统的逐步操作
- 绕过具体锁具安全机制的详细攻击步骤
- 未授权进入建筑/车辆的方法
- 偷车或非法进入方法
- 绕过报警/防盗系统的方法
- 可直接用于犯罪的 step-by-step instructions

**替代表达**（用以下维度重述危险主题）：

- 概念解释（conceptual explanation）
- 风险说明（risk disclosure）
- 合法专业场景（licensed professional context）
- 培训/认证场景（training / certification context）
- 安全维护（safe maintenance）
- 产品选择（product selection）
- 故障诊断（fault diagnosis）
- 厂商/专业人员建议（manufacturer / professional guidance）

---

## 6. 初始风险结论（供 Phase 1 决策）

1. **Locktool 应采用「专业锁匠工具 + 锁具技术教育资源」定位**，绝不以任何"破解/偷窃"导向词汇营销。
2. **产品分级的硬边界**：B 类（lock picks/tension/decoding）可做但必须合规定位；C 类（汽车防盗绕过、immobilizer 破解、covert entry）默认人工审核；D 类彻底排除。
3. **法域矩阵需补全**：US 逐州、UK 分地区、Canada/AU 分省州、EU 例外国（匈牙利）、以及 automotive 类目在所有法域的高风险单独评估。
4. **内容红线**：Knowledge Hub 只做"原理科普 + 选择 + 维护 + 培训"，绝不写攻击步骤。

> 下一步（Phase 1 内）：补全 Jurisdiction Matrix 的 [UNKNOWN] 项（优先 US 州法、UK、Canada/AU、EU 例外），并针对 automotive key programming 单独做一份 C 类高风险专项评估。

---

## 附：本文件引用信源（当前）

- Wikipedia — "Lock picking"（美/英/德/EU/匈牙利法条概述）
- worldpopulationreview.com — "Lockpick Laws by State 2026"（美国州法全表）
- toool.us — "Lockpicking Laws"（Open Organization of Lockpickers，含州法原文引注）
- unitedlocksmith.net — "Lock Pick Laws, Rules And Regulations"（TN/MS 最严格州案例分析）
- lockpickings.com — "Are Lock Pick Sets Illegal"（西欧/北欧/UK/NZ/AU 概述）

> 以上为二手/聚合信源，正式发布前需以官方政府/海关/监管机构原文为准。
