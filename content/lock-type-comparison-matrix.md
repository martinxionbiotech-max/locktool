---
title: "Lock Type Comparison Matrix: Mechanism, Combination Count, Manipulation Resistance, and Use Cases"
description: "Authoritative reference matrix comparing 6 lock types by mechanism, combination count, tolerance, manipulation resistance, and fitting use cases — sourced from manufacturer and standards data."
---

# Lock Type Comparison Matrix: The Single Reference Table

> 项目：Locktool · Reference
> 类型：原创数据资产（Normalized Data Asset）
> 所属 Hub：全站参考（跨 Hub）
> 主实体：`https://locktool.com/entity/lock#entity`
> 状态：PUBLISHED
> 研究日期：2026-09-12
> 信源层级：Tier 1（Abloy 官方 / Allegion 官方 / UL / ScienceDirect）+ Tier 2（锁匠行业权威）

---

## Quick Answer

**一句话：这张表把全站分散在 20+ 篇文章里的锁型机制数据，收敛成一张可引用的单一对照。** 每一格数字都标注来源等级 `[F]`（来源事实）或 `[D]`（行业推导），不混同、不编造。

它回答的不是「哪种锁最安全」，而是「六种锁型在**阻挡机制 / 组合数 / 公差 / 抗操纵 / 抗暴力 / 失效模式**六个维度上各自站在哪里」——安全决策要看威胁模型，而不是挑组合数最大的那行。

---

## Why This Matrix Exists

网络上散落着无数「XX 锁 vs YY 锁哪个安全」的文章，但它们普遍有两个问题：

1. **拿不可比的数字横向对比**——把 pin tumbler 的「5 销 8,200 组合」和 disc detainer 的「19 亿组合」放在一起比，却忽略两者失效模式完全不同（撞销 vs 逐片操纵）。
2. **把单一维度当成「安全」的全部**——抗撬 ≠ 抗钻 ≠ 抗暴力，混淆这三个维度是外行最常见、也最危险的错误。

这张表的目标是：**把机制工程特性对照，做成可引用的单一权威资产**。

> ⚠️ **使用边界**：本表是「机制工程特性」的对照，不是「安全等级排行」。真正的安全决策要看威胁模型（防谁、防什么），而不是挑组合数最大的那行。

---

## 主矩阵：6 种锁型 × 6 个关键维度

| 锁型 | 阻挡机制 | 典型组合数 | 组件公差 | 抗操纵（manipulation） | 抗暴力/抗钻 | 典型应用 |
|---|---|---|---|---|---|---|
| **Wafer** | 单片扁平叶片（方孔让钥匙穿过） | 低（4 片 × 4 深度 = 256 `[D]`；5 片 × 5 深度 = 3,125 `[D]`） | 松（冲压，1.2–1.5 mm 厚 `[F]`） | **最低**（最易 rake/jiggler）`[F]` | 低 | 柜子、抽屉、储物柜、办公家具、老式车门 |
| **Pin Tumbler** | 成对销钉（key pin + driver pin）+ 弹簧 | 5-pin 10 深度 = 100,000 理论；商用 **30k–50k** `[D]` | 紧（±0.001" / 0.025 mm `[F]`） | 低–中（可装 spool/serrated 销升级） | 中 | 住宅门、deadbolt、大多数挂锁 |
| **Dimple** | 侧面销钉（键面销，非边缘） | 中高（多排销 + 侧面定位） | 中–紧 | 中–高（抗 feeler pick，但有 snap 攻击弱点） | 中 | 中高端门锁、多用途 cylinder |
| **Tubular** | 径向排布销钉（放射状） | 中（7 销 × 4 深度 = 16,384 `[D]`，实用更少） | 中 | **被高估**（专用工具普遍，比外行以为的更易开）`[D]` | 中 | 自动售货机、自行车锁、投币柜 |
| **Lever** | 杠杆片 + bolt stump | 中（5-lever 是英国 BS3621 门槛） | 中 | 高（false notches + curtain + relocker 时） | 中–高 | 英国前门、保险柜、高端柜门 |
| **Disc Detainer** | 旋转盘片（侧面 driver 对齐 + sidebar） | **最高**（Abloy Protec2 ≈ **19–19.7 亿** `[F]`） | 紧（精密车削盘片） | **最高**（机械锁中，DBS + false gates） | 高（全硬化钢外壳） | 高安保挂锁、自行车、ATM、关键基础设施 |

> 🔴 **关键纠偏（2026-09-12）**：Abloy Protec2 的组合数是 **19–19.7 亿**，不是「1.9 亿」。11 片盘片 × 7 个切角 = 7¹¹ ≈ 19.8 亿理论组合；Abloy 官方口径「19 亿」，Locksmith Ledger 报「19.7 亿」。本页早期版本把它少写了一个数量级（「1.9 亿」），现已纠正。

---

## 两张不可混用的「等级」表

### 机械锁抗操纵等级 —— UL 768（保险柜组合锁）

| Group | 含义 | 抗操纵能力 |
|---|---|---|
| Group 2 | 基础 | 普通抵抗（多数 RSC 住宅保险柜最低要求） |
| Group 2M | 抗操纵 + 抗辐射 | 中级 |
| Group 1 | 高级抗操纵 | 高（商用/金库） |
| Group 1R | 最高 + 抗辐射（X 光） | 最高（唯一满足 DEA I/II 类管制物合规） |

> UL 768 **只测「抗操纵/解码」**（dial-reading、X-ray、manipulation），**不测抗暴力入侵**。柜体抗暴力是另一套 UL 687（见下）。

### 电子锁高安全认证 —— UL 2058 Type 1

- 覆盖攻击向量：ESD / 电压注入 / RF 攻击 + 物理操纵 + 耐久测试。
- Type 1 电子锁组合数可达 **100 万** `[F]`，高于 Group 2 机械锁——但**「猜码攻击」不是现实威胁**，钻/撬才是，而那要看柜体。
- ⚠️ **不能拿 UL 2058 Type 1 和 UL 768 机械锁直接比等级**——两套尺子测的东西不同。

### 保险柜柜体抗暴力等级 —— UL 687

| 等级 | 含义 | 关键纠正 |
|---|---|---|
| RSC | Residential Security Container | 住宅最低标准 |
| TL-15 | 抗 15 分钟净工具时间 | 见下方纠偏 |
| TL-30 | 抗 30 分钟净工具时间 | 见下方纠偏 |
| TRTL | 抗工具 + 抗 torch（火焰） | 最高 |

> 🔴 **关键纠偏**：UL 687 的「净工具时间」（net working time）≠ 真实破门时间。TL-30 的 30 分钟是「专家 + 专门工具」的净操作时间，实际破门（含观察、换工具、休息）远超 30 分钟。切勿望文生义。

---

## 论「组合数」为什么不能单独决定安全

| 锁型 | 组合数 | 失效模式 | 为什么不能比 |
|---|---|---|---|
| Pin Tumbler 5-pin | ≈ 8,200 `[F]`（或 30k–50k `[D]`） | 撞销（bump）/ 撬（pick） | 靠「撞动销钉对齐剪切线」 |
| Abloy Protec2 | ≈ **19 亿** `[F]` | 逐片操纵（猜盘片角度） | 靠「逐盘对准 sidebar」 |

两个数字差 4 个数量级，但**失效模式完全不同**：pin tumbler 是「把销钉撞到剪切线」，disc detainer 是「把每片盘片转到正确角度」。前者有 bump key 这种快速通用攻击，后者基本免疫 bump（无销钉可撞）`[F]`。

结论：**「组合数」只衡量「随机试钥匙」的成本，不代表「攻击者花时间操纵」的难度。** 横向对比要同时看失效模式 + 公差 + 安全销/false gates + keyway 限制 + 外壳硬化，缺一不可。

---

## 失效模式对照（选型常被忽略的维度）

| 锁型 | 主要失效模式 | 现场症状 |
|---|---|---|
| Wafer | 软质冲压叶片变形；弹簧疲劳；松公差钥匙磨损 | 错误钥匙也能转；叶片卡死 |
| Pin Tumbler | 弹簧疲劳；销钉尖端/驱动销磨损；腔体积垢 | 操作发粘；钥匙时灵时不灵 |
| Dimple | 伸缩销卡阻（积灰）；键面磨损；Euro 缸体 snap | 内销发「咯吱」；缸体前段断裂 |
| Tubular | 弹簧疲劳；销尖磨损；圆柱钥匙变形 | 钥匙摇晃才能转 |
| Lever | 杠杆弹簧疲劳；gate/stump 磨损；bit 钥匙磨损 | 螺栓发紧；钥匙抬不满杠杆 |
| Disc Detainer | 盘片/gate 磨损（Abloy AWS 抗磨系统缓解 `[F]`）；sidebar 磨损 | 转动渐松；反馈变钝 |

> 耐用性也有标准可依：**EN 1303** 把 cylinder 耐用性分为 grade 4（25,000 次）、5（50,000 次）、6（100,000 次）`[F]`。整锁（lockset）耐用性则看 ANSI/BHMA 等级，见标准 Hub。

---

## The Author's Take

**Position（立场）**：这张矩阵我刻意做成了「对照」而不是「排行」——因为锁安全不是一条从「差」到「好」的单线，而是一个多维空间。

**Reasoning（论证）**：
1. 同一个锁，在「防顺手开」的抽屉上是完美方案，在「防专业撬」的住宅门上就是漏洞——排行表会掩盖这个「场景决定对错」的本质。
2. 我最头疼的是「组合数」这一列：因为它最容易懂，也最容易误导。19 亿听起来「完爆」8,200，但 Abloy Protec2 的敌人从来不是「拿钥匙逐个试」的人，而是「花三天逐盘操纵」的人——后者根本不看组合数。
3. 所以我坚持在表里并列「失效模式」这一列，宁可让读者觉得「怎么没有简单排行榜」，也不给你一个会害死人的假答案。

**Disclosure（披露）**：以上是机制工程特性 + 公开规格数据的专业判断，非实测，属本人观点而非经验证事实。抗撬时间这类不可验证的量化断言，本页全站不做。

---

## FAQ

**这张表能直接拿来选锁吗？**
不能直接照抄，能用来缩短决策。先回答「防谁、防什么」（威胁模型），再到对应维度上找匹配的锁型。

**为什么没有「安全性综合得分」这一列？**
因为「安全性」不是可加总的单一标量。抗撬、抗钻、抗暴力、耐受性互不替代，强加一个总分会掩盖关键差异。

**组合数最高的锁就最安全吗？**
不是。组合数只衡量「随机试钥匙成本」，不衡量「操纵攻击难度」。见上表「失效模式」列。

**Abloy Protec2 到底有多少组合？**
约 **19 亿**（11 片盘片 × 7 个切角 = 7¹¹ ≈ 19.8 亿理论；官方口径「19 亿」，行业报道「19.7 亿」），不是「1.9 亿」。

---

## Sources（官方/一手优先）

- [Abloy — ABLOY PROTEC2](https://www.abloy.com/au/en/products/keying-platforms/abloy-protec2)（官方，访问 2026-09-12）— 「19 亿理论组合」、DBS、抗 bump、AWS 抗磨系统、专利至 2031。
- [Locksmith Ledger — Abloy Protec2](https://www.locksmithledger.com/locks/article/12438396/abloy-protec2-the-ultimate-locking-solution)（访问 2026-09-12）— 11 盘片、UL 437、「19.7 亿不同组合」。
- [Allegion (Schlage) — MACS](https://kc.allegion.com/kb/article/what-is-the-maximum-adjacent-cut-specification-or-macs)（官方，访问 2026-09-12）— Schlage Conventional/Full Size MACS=7；Small Format 无 MACS。
- [Firgelli Automations — Pin Tumbler Lock](https://www.firgelliauto.com/blogs/mechanisms/pin-tumbler-lock)（访问 2026-09-12）— 10 深度、100,000 理论 / 30k–50k 商用、±0.001" 公差。
- [Firgelli Automations — Wafer Tumbler Lock](https://www.firgelliauto.com/blogs/mechanisms/wafer-tumbler-lock)（访问 2026-09-12）— 叶片厚 1.2–1.5 mm、5 片 × 5 深度 = 3,125。
- [Lockwiki — Abloy Protec](https://www.lockwiki.com/index.php/Abloy_Protec)（访问 2026-09-12）— 9/11 盘片、DBS、EN 1303、UL 437。
- [Lockwiki — EN 1303](https://www.lockwiki.com/index.php/EN_1303)（访问 2026-09-12）— 耐用性 grade 4/5/6、抗攻击 grade 0/A/B/C/D。
- [toool.nl — Abloy Part III: Protec](https://toool.nl/images/8/8a/Abloypart3.pdf)（访问 2026-09-12）— 11 盘片、7 个切角 0–6、理论 19.7 亿组合。
- [ScienceDirect](https://www.sciencedirect.com/) — Tumbler Mechanism（pin tumbler 5-pin ≈ 8,200 组合数）。
- Safe & Vault Store — Mechanical vs Electronic vs Biometric（UL 768 四 Group、UL 2058 Type 1、ESD/RF 攻击向量）。

> 组合数与等级均来自上述信源，非我方自制。未实测抗撬时间，本表不做这类不可验证的量化断言。

---

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上来源均为第三方权威来源与制造商公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导/经验）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联（内部链接规划）

- → Pillar：[Pin Tumbler vs Wafer vs Disc Detainer](technology/pin-tumbler-vs-wafer-vs-disc-detainer.md)
- → [EN 1303 Decoded](standards/en-1303-decoded.md)（欧标锁芯 8 位码）
- → [ANSI/BHMA Grades Decoded](standards/ansi-bhma-grades-decoded.md)（门锁 Grade 1/2/3）
- → [Safe Burglary Ratings Decoded](vault/safe-burglary-ratings-decoded.md)（UL 687 RSC/TL-15/TL-30）
- → [Safe Lock Types Explained](vault/safe-lock-types-explained.md)（UL 768 Group + UL 2058 Type 1）
- → Entity：`https://locktool.com/entity/lock#entity` / `https://locktool.com/entity/pin-tumbler#entity` / `https://locktool.com/entity/wafer#entity` / `https://locktool.com/entity/disc-detainer#entity`
