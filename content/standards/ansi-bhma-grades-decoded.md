---
title: "ANSI/BHMA Grade 1, 2, and 3 Decoded: What Door Lock Grades Actually Measure"
description: "ANSI/BHMA lock grades decoded: what Grade 1, 2, 3 actually measure — cycles, impact, strength, and torque per A156.2/A156.13/A156.5 — and why higher grade ≠ pick-proof."
---
# ANSI/BHMA Grade 1, 2, and 3 Decoded: What Door Lock Grades Actually Measure

> 项目：Locktool · Content
> 类型：Standards Cluster（模板 B/E）
> 所属 Hub：Standards & Compliance Hub（/standards/）
> 主实体：`https://locktool.com/entity/ansi-bhma#entity`、`https://locktool.com/entity/door-lock#entity`
> 状态：DRAFT（v0.2 工程参数升级）
> 研究日期：2026-09-12

---

## Quick Answer

ANSI/BHMA 门锁等级（Grade 1、2、3）排序是 **Grade 1 最高、Grade 3 最低**，由 BHMA 制定、经 ANSI 采纳，通过**循环寿命（cycle）、撞击（impact）、强度/扭矩（strength）**三类测试给门锁评级。**Grade 测的是"耐用 + 抗暴力破坏"，不是"抗撬/抗钻"**——Grade 1 是商用/机构标准，Grade 3 是住宅标准。

一句话：**Grade 回答"这扇门能用多久、多抗砸"，不回答"多难撬"。**

---

## Definition

**ANSI/BHMA Grade**（门五金等级）：由 BHMA（Builders Hardware Manufacturers Association）在 ANSI/BHMA A156 系列标准中定义、由认可实验室测试的门五金**性能分级**。每类五金有独立分册，测试维度包括 cycle（循环寿命）、operational（操作性）、strength（强度/扭矩）、security（抗撞击/抗破坏）、material、finish。Grade 1 / 2 / 3 代表**逐级递减的测试阈值**，Grade 1 最高。

**关键分册与锁型对应**（`[F]`）：

| 分册 | 覆盖 | 说明 |
|---|---|---|
| **A156.2** | Bored / cylindrical locks（圆筒锁、杠杆锁） | 最常见的旋钮/杠杆锁 |
| **A156.13** | Mortise locks（插芯锁） | 商用主流，含 warped door 测试 |
| **A156.5 / A156.36** | Auxiliary locks（deadbolt 等辅助锁） | deadbolt 锁芯与辅助锁 |
| **A156.3** | Exit devices（逃生/防火逃生推杆） | 逃生推杆，含 panic/fire exit |
| **A156.30** | High Security Cylinders（高安全锁芯） | 高安全锁芯，引用 UL 437 |

---

## 三个等级的核心参数矩阵（按锁型分列）

> ⚠️ 先说明：ANSI/BHMA 的 cycle 阈值**随锁型不同是几套数字**，且随标准版本迭代会有差异。下表是"常见口径"，采购时以 **BHMA Certified 产品目录（CPD）** + 型号级报告为准。

### 循环寿命（Cycle，`[F]`，典型口径）

| 锁型 | Grade 1 | Grade 2 | Grade 3 |
|---|---|---|---|
| Bored / cylindrical（A156.2） | 800,000（2003 版；部分现行来源 1,000,000） | 400,000 | 200,000 |
| Mortise（A156.13） | 1,000,000 | 800,000 | 400,000 |
| Deadbolt（A156.5 / A156.36） | 250,000 | 150,000 | 100,000 |

### 撞击抵抗（Impact，deadbolt 锤击，`[F]`）

| 维度 | Grade 1 | Grade 2 | Grade 3 |
|---|---|---|---|
| 锤击次数（约 75 lbf-ft / 100 J 每次） | 10 次 | 5 次 | 2 次 |

### 强度 / 扭矩（Strength，`[F]`）

| 维度 | Grade 1 | Grade 2 | Grade 3 |
|---|---|---|---|
| 门撞击 / 负载（weight test） | ~360 lbf | ~250 lbf | ~150 lbf |
| 杠杆开锁扭矩（可及性，各等级一致） | ≤ 28 in-lbf | ≤ 28 in-lbf | ≤ 28 in-lbf |
| 关门闭锁力（各等级一致） | ≤ 4.5 lbf | ≤ 4.5 lbf | ≤ 4.5 lbf |

### 其他关键参数（`[F]`）

- **Deadbolt 锁舌伸出（throw）**：Grade 1 和 Grade 2 要求 **1 英寸（25.4 mm）** 最小伸出。
- **Exit devices（A156.3）**：释放力 ≤ 15 lbf；Grade 1 = 500,000 cycles。

---

## 一个必须诚实说明的"口径差异"

你自己去搜，会发现**不同来源给出的 cycle 数字不一样**（Grade 1 锁具有写 800k、有写 1M；mortise 有写 800k、有写 1M）。这不是哪个来源错了，而是几个原因叠加：

1. **标准版本迭代**——A156.x 系列持续更新，阈值会调整（2003 版与现行版不同）。
2. **锁型不同**——mortise、cylindrical、deadbolt 各有各的 cycle 阈值，**不能拿 deadbolt 的 250k 去比锁具的 800k**。
3. **"cycle" 定义差异**——"跌破性能" vs "完全失效"，口径不同。

**结论**：认准"**Grade 1 > 2 > 3，且 Grade 测的是耐用 + 抗暴力破坏**"这个框架就好，别死记某个数字。采购以 **BHMA CPD** + 型号级报告为准。

---

## Grade 等级的两个常见误区

### 误区 1：Grade 高 = 抗撬强
**错。** Grade 测的是**耐用（cycle）和抗暴力破坏（impact/strength）**，不是抗撬（pick）或抗钻。一个 Grade 1 商用锁抗锤击很牛，但抗撬不抗撬，要看有没有 security pins、paracentric keyway、restricted keyway——这些是 Grade 不测的维度（要抗撬/抗钻，去看 UL 437 或 A156.30 高安全锁芯）。

### 误区 2：Smart Lock 的 Grade = 它的安全等级
**半对。** 智能锁的**电子功能**（键盘、指纹、App）和它的 **ANSI 机械认证是分开的**。锁体、bolt 仍要过 cycle/冲击/强度测试，但"电子安全"（蓝牙破解、固件漏洞）不在 ANSI Grade 评估范围。多数住宅智能锁的**机械部分**是 Grade 3——住宅够用，但别把"带指纹"误当成"机械强度更高"。

---

## The Author's Take

**Position**：我的判断是——ANSI/BHMA Grade 是北美门锁最实用的"耐用性标尺"，但它被严重误读成"安全等级"了，这是选锁时最普遍的认知错位。

**Reasoning**：
1. **Grade 回答"能用多久、多抗砸"，不回答"多难撬"**——威胁是"有人撬锁/钻锁"，Grade 帮不了你，要去看 security pins、restricted keyway 和 UL 437/A156.30。威胁是"高流量门的锁会坏、会被踹开"，Grade 才是关键。
2. **住宅别盲目上 Grade 1**——Grade 1 是为每天几百次开合设计的，用在住宅卧室门是过度设计（贵且没必要）。Grade 3 对正常家庭门够用且经济。
3. **数字会变、框架不变**——别纠结 800k 还是 1M，记住"Grade 1 > 2 > 3，测耐用 + 抗暴力，分锁型看数字"就够用。真正下单时以 BHMA CPD 目录为准。

**Disclosure**：以上是基于 BHMA 标准公开说明 + 行业共识的专业判断，非认证机构结论，也不构成采购合规意见。

---

## FAQ

**ANSI Grade 1、2、3 哪个最高？**
Grade 1 最高（商用/机构），Grade 3 最低（住宅）。排序 Grade 1 > 2 > 3。

**Grade 高就代表抗撬强吗？**
不。Grade 测耐用 + 抗暴力破坏，不测抗撬/抗钻。

**住宅该选哪个 Grade？**
普通住宅 Grade 2–3 足够；高流量公共门才需要 Grade 1。

**为什么 deadbolt 的 cycle 比锁具少？**
deadbolt 是辅助锁，测试口径与主锁具不同（Grade 1 = 250k vs 锁具 800k–1M），不能直接比。

---

## Sources

- **ANSI/BHMA A156 系列** — BHMA（buildershardware.com）：A156.13 Mortise Locks（1,000,000 cycles、28 in-lbf 杠杆扭矩）、A156.36 Auxiliary Locks（Grade 1 deadbolt 250,000 cycles、1,350 lbf 测试）、A156.2 Bored Locks，访问 2026-09-12
- **ANSI blog** — ANSI/BHMA grade levels（cycle / operational / 28 in-lbf / 4.5 lbf），访问 2026-09-12
- Locksmith Ledger — ANSI/BHMA Standards for Residential Grade Hardware（A156.5-2001 范围、Grade 1=800k/2=400k/3=200k，2003 口径），访问 2026-09-12
- CDF Distributors — ANSI/BHMA Hardware Standards Guide（A156.2/A156.3/A156.5/A156.13 分册范围），访问 2026-09-12
- PDQ Locks — Grade 1 vs Grade 2（1,000,000 / 250,000 cycles、360/250 lbf），访问 2026-09-12

> cycle/impact 具体数字随标准版本和锁型变动；以 BHMA CPD + 型号级报告为准。

---

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。凡属我方推断/折减的结论，已在「The Author's Take」中明确标注「专业判断」，不混同于来源事实。

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上来源均为标准组织/制造商公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联

- → [Lock Security Standards Explained](lock-security-standards-explained.md)（Pillar，四体系对照）
- → [EN 1303 Decoded](en-1303-decoded.md)（欧标 8 位码对照）
- → [Pin Tumbler Lock Explained](../technology/pin-tumbler-lock-explained.md)（security pins 抗撬——Grade 不测的维度）
- → [Fire-Rated Door Hardware Explained](fire-rated-door-hardware-explained.md)（Grade 与防火门硬件的关系）
- → [ALOA Certification Levels](../certification/aloa-certification-levels.md)（标准如何进入锁匠资质）
- → Entity：`https://locktool.com/entity/ansi-bhma#entity` / `https://locktool.com/entity/door-lock#entity`
