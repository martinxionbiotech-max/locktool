---
title: "Lock Security Standards Explained: ANSI/BHMA, EN 1303, UL 437, and TS007"
description: "Lock security standards explained: ANSI/BHMA, EN 1303, UL 437, and TS007 compared as engineering parameter systems — what each measures, and why they don't convert."
---
# Lock Security Standards Explained: ANSI/BHMA, EN 1303, UL 437, and TS007

> 项目：Locktool · Content
> 类型：Standards Pillar（模板 B/E）
> 所属 Hub：Standards & Compliance Hub（/standards/）
> 主实体：`https://locktool.com/entity/lock-standard#entity`、`https://locktool.com/entity/ansi-bhma#entity`、`https://locktool.com/entity/en-1303#entity`、`https://locktool.com/entity/ul-437#entity`
> 状态：DRAFT（v0.2 工程参数升级）
> 研究日期：2026-09-12

---

## Quick Answer

锁具安全等级**没有一个"全球统一"的标尺**，而是几套**平行、不可直接换算**的体系：**北美看 ANSI/BHMA Grade（1–3，测耐用 + 抗暴力破坏），欧洲看 EN 1303 的 8 位码（逐维编码，含钥匙安全 1–6 级与攻击抵抗 0–D 级），英国叠看 TS007 星级（专补 EN 1303 不测的 lock snapping），北美高安全锁看 UL 437（攻击抵抗分钟数）。**

一句话：**Grade 测"能用多久、多抗砸"，EN 1303 测"逐项体检"，TS007 测"抗折断"，UL 437 测"扛多久攻击"。四者测的不是同一件事，不能跨体系比大小。**

---

## Definition

**Lock security standard**（锁具安全标准）：由标准组织发布的、规定锁具/锁芯/门五金**性能测试方法与合格阈值**的规范性文件。它回答的不是"这把锁安不安全"的哲学问题，而是"在**定义的测试方法**下，这把锁通过了哪一档**可复现的阈值**"。

四套主体系各自的发布主体与版本：

| 标准 | 发布主体 | 地区 | 现行版本（截至 2026-09） |
|---|---|---|---|
| **ANSI/BHMA A156 系列** | BHMA（Builders Hardware Manufacturers Association，经 ANSI 采纳） | 北美 | A156.2 / A156.13 / A156.36 等分册持续迭代 |
| **EN 1303** | CEN（欧洲标准化委员会） | 欧洲 | EN 1303:2015（英国采纳为 BS EN 1303:2015） |
| **TS007** | 英国锁具行业（Kitemark 认证体系） | 英国 | 现行 1–3 星体系 |
| **UL 437** | UL（Underwriters Laboratories） | 北美 | 现行攻击抵抗测试标准 |

> 本文关键阈值均来自标准原文/标准组织/权威解读，标注 `[F]`（事实）。凡属推断/折减的结论，在「The Author's Take」中标注为专业判断，不与来源事实混同。

---

## 四套体系到底在测什么（工程维度总表）

| 体系 | 核心测量维度 | 输出形式 | 商业含义（采购视角） |
|---|---|---|---|
| **ANSI/BHMA Grade** | 耐久（cycle）+ 强度/扭矩（strength）+ 撞击（impact） | Grade 1 / 2 / 3（1 最高） | "这扇门每天用多少次、抗不抗砸" → 决定买商用还是住宅 |
| **EN 1303** | 耐久 + 防火 + 腐蚀/温度 + **钥匙安全** + **攻击抵抗** | 8 位数字码（逐维分档） | "逐项对比锁芯" → 决定买哪把锁芯、盯哪一位数字 |
| **TS007** | 抗 snap（折断）为主 + pick/bump/drill/extraction | 1 / 2 / 3 星 | "uPVC 门会不会被折断" → 决定要不要上 3 星 |
| **UL 437** | 8 种攻击的**抵抗分钟数** | 通过 / 不通过（Listed） | "高安全锁芯" → 决定要不要为抗钻/抗撬上 UL 437 锁芯 |

**关键认知（纠偏）**：这四者**不在同一坐标系**。ANSI Grade 基本不测抗撬/抗钻（那是 security pins / restricted keyway 的事）；EN 1303 不测 lock snapping（那是 TS007 的事）；UL 437 测攻击时长但**本身不定义"高安全锁"**——它被 BHMA/ANSI **A156.30（High Security Cylinders）** 等高安全标准引用。

---

## 各标准的本质区别（工程参数级）

### ANSI/BHMA（北美门锁主流）——测"耐用 + 抗暴力"

由 BHMA 制定、经 ANSI 采纳。核心测**三类事**，且**分锁型用不同分册**：

| 分册 | 覆盖 | Grade 1 循环寿命（典型） |
|---|---|---|
| **A156.2** | Bored / cylindrical locks（圆筒锁、杠杆锁） | 800,000 cycles（2003 版口径；部分现行来源引 1,000,000）`[F]` |
| **A156.13** | Mortise locks（插芯锁） | 1,000,000 cycles `[F]` |
| **A156.5 / A156.36** | Auxiliary locks（deadbolt 等辅助锁） | 250,000 cycles（deadbolt）`[F]` |
| **A156.3** | Exit devices（逃生/防火逃生推杆） | 500,000 cycles `[F]` |

1. **Cycle（循环寿命）**：机器反复开合多少次才失效。
2. **Impact（撞击）**：bolt 抗多少次锤击——deadbolt 的 Grade 1 = 10 次、Grade 2 = 5 次、Grade 3 = 2 次（约 75 lbf-ft / 100 J 每次）`[F]`。
3. **Strength（强度/负载）**：latch 抗多少磅拉力、lever 抗多少扭矩——杠杆开锁扭矩 ≤ 28 in-lbf、关门闭锁力 ≤ 4.5 lbf（可及性要求）`[F]`。

**关键认知**：Grade 测的是"耐用 + 抗暴力破坏"，**不是抗撬/抗钻**。详见 [ANSI/BHMA Grade 1/2/3 Decoded](ansi-bhma-grades-decoded.md)。

### EN 1303（欧标锁芯）——8 位码逐维体检

用**一个 8 位数字编码**概括 Euro cylinder 锁芯，每位对应一个维度。真正"有区分度"的是这几位：

- **Digit 2 耐久**：grade 4/5/6 = 25,000 / 50,000 / 100,000 cycles `[F]`。
- **Digit 6 腐蚀/温度**：grade 0/A/B/C；grade C = 高抗腐蚀 + -25°C 至 +65°C 工作 `[F]`。
- **Digit 7 钥匙安全（1–6 级）**：min effective differs 从 100（grade 1）到 100,000（grade 6）；movable detainers 从 2 到 6 个 `[F]`。
- **Digit 8 攻击抵抗（0–D 级）**：抗钻 net drilling time、抗凿击、抗扭、抗拔芯，D 最高 `[F]`。

完整参数矩阵见 [EN 1303 Decoded](en-1303-decoded.md)。

### TS007（英国星级）——补 EN 1303 的 snap 盲区

EN 1303 的著名盲区是**不测 lock snapping（锁芯折断）**——这是英国 uPVC/复合门 Euro cylinder 最常见的攻击方式。TS007 专门补洞：

- **3 星锁芯**：单独抗 snap、pick、bump、drill、plug extraction。
- **1 星锁芯 + 2 星把手**：组合达到 3 星等效。
- 3 星锁芯的测试引用 BS 3621、BS EN 1303、PAS 24 的要求 `[F]`。

> 注意：TS007 是英国体系，与 EN 1303 互补而非替代。

### UL 437（北美高安全锁芯）——攻击抵抗分钟数

UL 437 测锁对抗**8 种攻击的时钟时长**（door locks/cylinders 口径）`[F]`：

| 攻击 | 抵抗时长 |
|---|---|
| Picking | 10 分钟 |
| Impressioning | 10 分钟 |
| Forcing / Drilling / Sawing / Prying / Pulling / Punching | 各 5 分钟 |

外加耐久测试（10,000 次循环 + 50 次换芯/换钥匙）。

**重要纠偏**（Lockwiki 明确指出）：**UL 437 不定义美国的"高安全锁"标准**——它是攻击抵抗测试，被 BHMA/ANSI **A156.30（High Security Cylinders）** 等高安全标准引用。厂商把 "UL 437 listed" 当营销词很普遍，但它在标准层面不是"高安全"的裁决者。

---

## 一个必须诚实说明的"数字口径会打架"

不同来源对 ANSI/BHMA 的 cycle 数字有差异（Grade 1 锁具有写 800k、有写 1M）。原因是真实的：

1. **测试标准版本迭代**（A156.x 系列持续更新，2003 版与现行版阈值不同）；
2. **锁型不同**（mortise vs cylindrical vs deadbolt 的 cycle 阈值是**三套数字**，不能拿 deadbolt 的 250k 去比锁具的 800k）；
3. **"cycle" 定义差异**（跌破性能 vs 完全失效，口径不同）。

**结论**：读标准认"等级框架 + 测试维度"，不要死记具体数字。采购以 **BHMA Certified 产品目录（CPD）** + 型号级测试报告为准。

---

## The Author's Take

**Position**：我的判断是——普通人选锁最该建立的不是"背出每套标准的数字"，而是**分清每套标准到底在测什么**。四套体系里，最容易用错的是把 ANSI Grade 当"安全等级"、把 "UL 437 listed" 当"高安全认证"。

**Reasoning**：
1. **ANSI Grade 测"耐用抗砸"，不测"抗撬"**——一个 Grade 1 商用锁抗暴力很牛，但抗撬要看有没有 security pins / restricted keyway，Grade 本身不保证。威胁是"撬/钻"的话，你要看的是 UL 437 或 A156.30，不是 Grade。
2. **EN 1303 的 8 位码是锁芯的"体检报告"**——与其纠结"这是不是好锁"，不如读 Digit 7（钥匙安全）和 Digit 8（攻击抵抗）。这是欧洲体系最大的实用价值。
3. **"UL 437 listed" 是营销重灾区**——它测攻击抵抗时长，且不定义"高安全"。别看到 UL 437 就自动等于"顶级安全"。

**Disclosure**：以上是基于各标准公开说明 + Lockwiki / 标准组织 / 制造商技术资料的专业判断，非第三方实测认证结论，也不构成采购合规意见。

---

## FAQ

**ANSI Grade 和 EN 1303 能直接比吗？**
不能。ANSI Grade 测耐用/抗破坏，EN 1303 是 8 位码逐维编码，口径不同。

**UL 437 是"高安全锁"标准吗？**
严格说不是。它测攻击抵抗时长，不定义美国"高安全锁"，被 A156.30 等高安全标准引用。

**TS007 和 EN 1303 什么关系？**
TS007 是英国星级标准，补 EN 1303 不测 snap（锁芯折断）的盲区，两者互补。

**住宅选锁认什么？**
北美看 ANSI/BHMA Grade 2–3，欧洲看 EN 1303 码（盯 Digit 7/8），英国叠看 TS007 星级。

---

## Sources

- **ANSI/BHMA A156 系列** — BHMA（buildershardware.com，A156.2 / A156.5 / A156.13 / A156.36 分册说明），访问 2026-09-12
- **EN 1303:2015** — CEN；权威解读见 [Lockwiki — EN 1303](https://www.lockwiki.com/index.php/EN_1303)（8 位码逐位、Digit 6/7/8 完整阈值表），访问 2026-09-12
- **UL 437** — [Lockwiki — UL 437](https://www.lockwiki.com/index.php/UL_437)（8 种攻击分钟数、耐久测试、"不定义高安全"纠偏），访问 2026-09-12
- **TS007** — Master Key Systems / Locksmiths.co.uk（1/2/3 星体系、3 星引用 BS 3621 / BS EN 1303 / PAS 24），访问 2026-09-12
- **A156.30 High Security Cylinders** — BHMA（buildershardware.com，机械 + 电气高安全锁芯），访问 2026-09-12
- ANSI blog — ANSI/BHMA grade levels（cycle / operational / 28 in-lbf 杠杆扭矩），访问 2026-09-12

> 具体测试数值随标准版本与锁型变动；采购以 BHMA CPD + 型号级测试报告为准。

---

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。凡属我方推断/折减的结论，已在「The Author's Take」中明确标注「专业判断」，不混同于来源事实。

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上来源均为标准组织/权威解读/制造商公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联

- → [EN 1303 Decoded](en-1303-decoded.md)（8 位码逐位参数矩阵）
- → [ANSI/BHMA Grade 1/2/3 Decoded](ansi-bhma-grades-decoded.md)（Grade 参数矩阵）
- → [Fire-Rated Door Hardware Explained](fire-rated-door-hardware-explained.md)（NFPA 80 / UL 10C）
- → [Pin Tumbler Lock Explained](../technology/pin-tumbler-lock-explained.md)（security pins 抗撬——Grade 不测的维度）
- → [Disc Detainer Locks Explained](../technology/disc-detainer-locks-explained.md)（高安全锁芯机制）
- → [How to Become a Locksmith](../certification/how-to-become-a-locksmith.md)（标准如何进入职业资质）
- → Entity：`https://locktool.com/entity/lock-standard#entity` / `https://locktool.com/entity/ansi-bhma#entity` / `https://locktool.com/entity/en-1303#entity` / `https://locktool.com/entity/ul-437#entity`
