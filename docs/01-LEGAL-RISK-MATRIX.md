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
| US | lock picks / pick sets | 联邦无统一禁止；各州不一——**多数州合法需"意图"导向**，但 MN/MS/NV/OH/VA 将 possession 视为 prima facie evidence（需自证非犯罪意图），TN 另加"未持证不得营利从事锁匠"限制；IL 禁 bump keys | 无联邦进口禁令（工具类正常通关） | 多数州需"合法意图"；MS 需"非隐蔽"（隐蔽持有即 prima facie）；NV/OH/VA 需自证无犯罪意图 | 禁止面向盗窃/未授权进入的表述 | 中 | B/C | worldpopulationreview (2026), toool.us, Wikipedia lock_picking（CA Penal Code §466 明确 burglary tools 需 intent） | 2026-09-11 |
| UK (England & Wales) | lock picks / burglary tools | **Theft Act 1968 s.25 "Going equipped"**：非居住地携带可用于 burglary/theft 的物件即构成犯罪；Crown Court 最高 **3 年监禁 + 无限罚金**（Magistrates 最高 12 个月，2022-05-02 后施行） | 无专门进口禁令，但销售/供应面向盗窃用途的工具受 CPS 追诉 | "not at place of abode" + 携带工具 + 可证明用于 burglary/theft 即成立；s.25(3) 若工具"made/adapted for"用途即推定故意 | 禁止 burglary 导向 | 中高 | B/C | legislation.gov.uk (s.25), cps.gov.uk, sentencingcouncil.org.uk | 2026-09-11 |
| UK (Scotland) | lock picks | **独立法律体系（Scots law）**，不受 Theft Act 1968 s.25（该条标 E+W，仅英格兰和威尔士适用）；苏格兰以**普通法 theft / housebreaking offenses** 追诉携带 burglary 工具的意图犯罪 | 无专门进口禁令 | 依苏格兰普通法：携带工具 + 意图入室/盗窃可诉；无成文"going equipped"对应条款 | 禁止 burglary / housebreaking 导向 | 中高 | B/C | sccjr.ac.uk（苏格兰刑事司法体系）, Wikipedia Scots law | 2026-09-11 |
| EU (general) | lock picks | **无欧盟统一法规**，刑法由各成员国自行处理；多数成员国不监管持有 | 低 | 低（Hungary 例外，公共场所持有禁止） | 一般；法国/意大利/西班牙强调"情境"判断 | 低-中 | B | Wikipedia lock_picking, multipick.com | 2026-09-11 |
| DE | lock picks | 合法——无专门法规；需物主许可；§202c StGB（"Hacker Paragraph"）仅在关联实际未经授权访问时才可罚；locksport 俱乐部普遍 | 低（工具自由买卖） | 低 | 一般（公开持锁需注意透明度/情境，避免"间谍式"隐蔽） | 低 | A/B | Wikipedia, multipick.com (§202c StGB) | 2026-09-11 |
| HU | lock picks | **EU 内特例**：`175/2003 (X.28.) Korm. rendelet` 禁止**公共场所持有**锁匠工具（家中持有合法） | 中高 | 高（公共场所持有归为"对公共安全特别危险的器具"） | 高 | 高 | C/D | Wikipedia（引 Jogtár 175/2003 Korm. rendelet） | 2026-09-11 |
| Canada | lock picks | 联邦《刑法》s.351(1) **"Possession of break-in instruments"**：无合法理由持有可用于破入场所/车辆/保险柜的工具且明知用途，即构成犯罪（可公诉，最高 **10 年**）；**锁匠工具合法持有，但与 crowbar 同类，需无犯罪意图** | 无联邦专门进口禁令 | s.351 需无犯罪意图；**Alberta 是唯一要求对 lockpick 持有注册的省份**；BC/Ontario **从事锁匠需 license**（Consumer Protection BC / Ontario Locksmiths Licensing Act 1996） | 禁止 break-in 导向 | 中 | B/C | laws-lois.justice.gc.ca (s.351 官方条文), Wikipedia | 2026-09-11 |
| AU | lock picks | 各州/领地独立立法，**无联邦统一法**；NSW 最严（strict liability，无需证明意图） | [REVIEW_REQUIRED] 需逐州核海关入境细则 | NSW s114(1)(b)（strict liability，最高 2/7 年）、VIC s49D（2 年）、QLD s425（3 年）、WA s407（3 年）、SA s21C（罚款$2,500 或 6 个月）、TAS s7B（50 penalty units或2年）、NT s57（$1,000/6个月）、ACT s315（going equipped）——多数需"lawful excuse"抗辩 | 禁止 burglary / housebreaking 导向 | 中高 | B/C | bareboneslockpicking.com（含各州法条表）, legislation（Crimes Act 1900 NSW 等） | 2026-09-11 |
| NZ | lock picks | 工具本身合法；Crimes Act 1961 s.233 **"possession of instrument for burglary"**：携带工具 + 意图用于 burglary 即犯罪，最高 **3 年** | 无专门进口禁令（可正常进口，见 LegalAdviceNZ 讨论） | 意图导向——只 pick 自己拥有的锁即安全 | 一般 | 中 | B | legislation.govt.nz (s.233 官方条文), Wikipedia | 2026-09-11 |
| automotive key programming / immobilizer tools | 高风险双用途；**UK 2024/2025 新法**新增"制造/供应/持有电子盗窃工具（relay attack / key programmer / clone 设备）"罪名，最高 **5 年**；US 由联邦 Vehicle Theft Prevention Standard（49 U.S.C. 33106）规范 immobilizer 性能要求 | [REVIEW_REQUIRED] UK 供应面向盗窃的 keyless 设备属新罪；US 无专门进口禁令但供应面向盗车的 programmer 涉刑 | 依用途区分：授权锁匠/经销商合法操作 vs 面向盗车的 supply 非法 | 禁止"绕过防盗/免钥匙偷车/image clone/relay attack"任何表述 | 高 | **C** | specialist-trackers.uk、gotyoucovered.com（UK 新法）、federalregister.gov | 2026-09-11 |

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

> 官方（一手，正式发布前优先引用）：

- **UK**: legislation.gov.uk — Theft Act 1968 s.25（Going equipped，标 E+W）；cps.gov.uk — Theft Act Offences 起诉指南；sentencingcouncil.org.uk — Going equipped 量刑指南
- **Canada**: laws-lois.justice.gc.ca — Criminal Code s.351/s.353（Possession of break-in instruments / 汽车万能钥匙）官方条文
- **Australia**: Crimes Act 1900 (NSW) s114(1)(b)；Summary Offences Act 1966 (Vic) s49D；Criminal Code (Qld) s425；Criminal Code (WA) s407；Summary Offences Act 1953 (SA) s21C；Police Offences Act 1935 (Tas) s7B；Criminal Code 2002 (ACT) s315；Summary Offences Act (NT) s57
- **New Zealand**: legislation.govt.nz — Crimes Act 1961 s.233（Possession of instrument for burglary）官方条文
- **US**: federalregister.gov — Exemption from Vehicle Theft Prevention Standard（49 U.S.C. 33106）；California Penal Code §466

> 二手/聚合（用以定位，不以之为法律结论）：

- Wikipedia — "Lock picking"（美/英/德/EU/匈牙利/加拿大/澳洲法条概述）
- worldpopulationreview.com — "Lockpick Laws by State 2026"（美国州法汇总）
- toool.us — "Lockpicking Laws"（Open Organization of Lockpickers）
- bareboneslockpicking.com — 澳洲各州法条对照表
- multipick.com / lockpickings.com — 德/EU/西欧法条概述
- sccjr.ac.uk — 苏格兰刑事司法体系（说明 Scots law 独立于 Theft Act 1968）

> ⚠️ 仍标记 [REVIEW_REQUIRED] 的项（AU 进口细则、automotive 供应新罪的具体实施），正式发布前须由相应法域资质律师复核。所有日期以文中 Last Checked 为准。
