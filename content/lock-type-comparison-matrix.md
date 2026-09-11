---
title: "Lock Type Comparison Matrix: Mechanism, Combination Count, Manipulation Resistance, and Use Cases"
description: "Authoritative reference matrix comparing 6 lock types by mechanism, combination count, manipulation resistance, and fitting use cases — sourced from manufacturer and standards data."
---

# Lock Type Comparison Matrix: The Single Reference Table

> 项目：Locktool · Reference
> 类型：原创数据资产（Normalized Data Asset）
> 所属 Hub：全站参考（跨 Hub）
> 主实体：`https://locktool.com/entity/lock#entity`
> 状态：PUBLISHED
> 研究日期：2026-09-11
> 信源层级：Tier 1（Abloy 官方 / UL / ScienceDirect / Wikipedia）+ Tier 2（锁匠行业权威）

---

## Why This Matrix Exists

网络上散落着无数「XX 锁 vs YY 锁哪个安全」的文章，但它们普遍有两个问题：

1. **拿不可比的数字横向对比**——把 pin tumbler 的「5 销 8,200 组合」和 disc detainer 的「1.9 亿组合」放在一起比，却忽略两者失效模式完全不同（撞销 vs 逐片操纵）。
2. **把单一维度当成「安全」的全部**——抗撬 ≠ 抗钻 ≠ 抗暴力，混淆这三个维度是外行最常见、也最危险的错误。

这张表的目标是：**把全站分散在 20+ 篇文章里的机制数据，收敛成一个可引用的单一权威对照**。每一格数字都标注来源等级 `[F]`（来源事实）或 `[D]`（行业推导/经验），不混同、不编造。

> ⚠️ **使用边界**：本表是「机制工程特性」的对照，不是「安全等级排行」。真正的安全决策要看威胁模型（防谁、防什么），而不是挑组合数最大的那行。

---

## 主矩阵：6 种锁型 × 5 个关键维度

| 锁型 | 阻挡机制 | 典型组合数 | 抗撬（manipulation） | 抗暴力/抗钻 | 典型应用 |
|---|---|---|---|---|---|
| **Wafer** | 单片扁平叶片（方孔让钥匙穿过） | 低（叶片少、深度档少） | **最低**（最易 rake/jiggler）`[F]` | 低 | 柜子、抽屉、储物柜、办公家具、老式车门 |
| **Pin Tumbler** | 成对销钉（key pin + driver pin）+ 弹簧 | 5-pin ≈ **8,200** 有效 `[F]`；Schlage 10 深度商用 **30k–50k** `[D]` | 低–中（可装 spool/serrated 销升级） | 中 | 住宅门、deadbolt、大多数挂锁 |
| **Dimple** | 侧面销钉（键面销，非边缘） | 中高（多排销 + 侧面定位） | 中–高（抗 feeler pick，但有 snap 攻击弱点） | 中 | 中高端门锁、多用途 cylinder |
| **Tubular** | 径向排布销钉（放射状） | 中（7–8 销，深度档少） | **被高估**（专用 pick 普遍，比外行以为的更易开）`[D]` | 中 | 自动售货机、自行车锁、投币柜 |
| **Lever** | 杠杆片 + bolt stump | 中（5-lever 是英国 BS3621 门槛） | 高（false notches + curtain + relocker 时） | 中–高 | 英国前门、保险柜、高端柜门 |
| **Disc Detainer** | 旋转盘片（侧面 driver 对齐 + sidebar） | **最高**（Abloy Protec2 ≈ **1.9–1.97 亿** `[F]`） | **最高**（机械锁中，DBS + false gates） | 高（全硬化钢外壳） | 高安保挂锁、自行车、ATM、关键基础设施 |

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
| Pin Tumbler 5-pin | ≈ 8,200 `[F]` | 撞销（bump）/ 撬（pick） | 靠「撞动销钉对齐剪切线」 |
| Abloy Protec2 | ≈ 1.9 亿 `[F]` | 逐片操纵（猜盘片角度） | 靠「逐盘对准 sidebar」 |

两个数字差 4 个数量级，但**失效模式完全不同**：pin tumbler 是「把销钉撞到剪切线」，disc detainer 是「把每片盘片转到正确角度」。前者有 bump key 这种快速通用攻击，后者基本免疫 bump（无销钉可撞）`[F]`。

结论：**「组合数」只衡量「随机试钥匙」的成本，不代表「攻击者花时间操纵」的难度。** 横向对比要同时看失效模式 + 公差 + 安全销/false gates + keyway 限制 + 外壳硬化，缺一不可。

---

## The Author's Take

**这张矩阵我刻意做成了「对照」而不是「排行」。** 因为锁安全不是一条从「差」到「好」的单线，而是一个多维空间——同一个锁，在「防顺手开」的抽屉上是完美方案，在「防专业撬」的住宅门上就是漏洞。

我做这个资产时最头疼的是「组合数」这一列：因为它最容易懂，也最容易误导。1.9 亿听起来「完爆」8,200，但 Abloy Protec2 的敌人从来不是「拿钥匙逐个试」的人，而是「花三天逐盘操纵」的人——后者根本不看组合数。所以我坚持在表里并列「失效模式」这一列，宁可让读者觉得「怎么没有简单排行榜」，也不给你一个会害死人的假答案。

（以上是机制工程特性 + 公开规格数据的专业判断，非实测。抗撬时间这类不可验证的量化断言，我全站不做。）

---

## FAQ

**这张表能直接拿来选锁吗？**
不能直接照抄，能用来缩短决策。先回答「防谁、防什么」（威胁模型），再到对应维度上找匹配的锁型。

**为什么没有「安全性综合得分」这一列？**
因为「安全性」不是可加总的单一标量。抗撬、抗钻、抗暴力、耐受性互不替代，强加一个总分会掩盖关键差异。

**组合数最高的锁就最安全吗？**
不是。组合数只衡量「随机试钥匙成本」，不衡量「操纵攻击难度」。见上表「失效模式」列。

---

## Sources（官方/一手优先）

- [Abloy](https://www.abloy.com/au/en/products/keying-platforms/abloy-protec2)（官方）— ABLOY PROTEC2（1.9 亿组合、DBS、SCEC SL3、专利至 2031）
- [Lockwiki](https://www.lockwiki.com/) — UL 768（Group 2/2M/1/1R）、UL 437、EN 1303、Abloy Protec（9/11 盘片）
- [ScienceDirect](https://www.sciencedirect.com/) — Tumbler Mechanism（pin tumbler 5-pin ≈ 8,200 组合数）
- Firgelli Automations — Pin Tumbler Lock（Schlage 10 深度、MACS=7、商用 30k–50k 组合）`[D]`
- Wikipedia — Pin tumbler lock / Wafer tumbler lock（机制 + master keying）
- Safe & Vault Store — Mechanical vs Electronic vs Biometric（UL 768 四 Group、UL 2058 Type 1、ESD/RF 攻击向量）

> 组合数与等级均来自上述信源，非我方自制。未实测抗撬时间，本表不做这类不可验证的量化断言。

---

> 研究日期：2026-09-11 · 访问日期：2026-09-11。以上来源均为第三方权威来源与制造商公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导/经验）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联（内部链接规划）

- → Pillar：Pin Tumbler vs Wafer vs Disc Detainer
- → EN 1303 Decoded（欧标锁芯 8 位码）
- → ANSI/BHMA Grades Decoded（门锁 Grade 1/2/3）
- → Safe Burglary Ratings Decoded（UL 687 RSC/TL-15/TL-30）
- → Safe Lock Types Explained（UL 768 Group + UL 2058 Type 1）
- → Entity：`https://locktool.com/entity/lock#entity` / `https://locktool.com/entity/pin-tumbler#entity` / `https://locktool.com/entity/wafer#entity` / `https://locktool.com/entity/disc-detainer#entity`
