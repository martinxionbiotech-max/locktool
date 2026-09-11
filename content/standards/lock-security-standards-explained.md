# Lock Security Standards Explained: ANSI/BHMA, EN 1303, UL 437, and TS007

> 项目：Locktool · Content
> 类型：Standards Pillar（模板 B/E）
> 所属 Hub：Standards & Compliance Hub（/standards/）
> 主实体：`#lock-standard`、`#ansi-bhma`、`#en-1303`、`#ul-437`
> 状态：DRAFT
> 研究日期：2026-09-11

---

## Direct Answer

锁具安全等级**没有一个"全球统一"的标尺**，而是**按地区分出几套平行体系**：

| 标准 | 地区 | 测什么 | 核心等级 |
|---|---|---|---|
| **ANSI/BHMA** | 北美 | 耐久 + 强度 + 撞击 | Grade 1–3（1 最高） |
| **EN 1303** | 欧洲 | 耐久 + 防火 + 钥匙安全 + 攻击抵抗 | 8 位数字编码 |
| **TS007** | 英国（补 EN 1303） | 抗 snap（锁芯折断）等攻击 | 1–3 星 |
| **UL 437** | 北美（高安全） | 8 种攻击的抵抗时间 | 通过/不通过 |

一句话：**北美看 Grade，欧洲看 8 位码，英国看星级，高安全锁看 UL 437。** 但每套标准的"测什么、怎么读"都不同，不能跨体系直接比大小。

---

## 各标准的本质区别

### ANSI/BHMA（北美门锁主流）
由 BHMA（Builders Hardware Manufacturers Association）制定，核心测**三件事**：

1. **Cycle（循环寿命）**：机器反复开合多少次才坏。
2. **Impact（撞击）**：bolt 抗多少次锤击。
3. **Strength（强度/负载）**：latum 抗多少磅拉力。

**Grade 1** 是商用/机构/高流量标准（寿命最高、抗撞击最强），**Grade 3** 是住宅标准。**关键认知**：Grade 测的主要是"耐用 + 抗暴力破坏"，不是"抗撬/抗钻"。

### EN 1303（欧标锁芯）
用**一个 8 位数字编码**概括锁芯表现，每位数字对应一个维度：

- Digit 2 耐久、Digit 4 防火、**Digit 7 钥匙安全（1–6 级）**、**Digit 8 攻击抵抗（grade 0/A/B/C/D）**、Digit 6 腐蚀/温度（-25°C 到 +65°C）等。

**关键认知**：EN 1303 的 8 位码能让你"逐项对比"锁芯，而不是看一个笼统的"等级"。它的 attack resistance（grade A/B/C/D）直接对应抗钻/抗机械攻击的**分钟级抵抗时长**。

### TS007（英国星级，补 EN 1303 的 snap 盲区）
EN 1303 的一个著名盲区是**不测 lock snapping（锁芯折断）**——这是英国 Euro cylinder 最常见被攻击方式。TS007 专门补这个洞：

- **3 星**：锁芯单独抗 snap、pick、bump、drill、plug extraction 五种攻击。
- **1 星 + 2 星把手**：1 星锁芯 + 2 星安全把手（escutcheon）组合，也能达到 3 星效果。

### UL 437（北美高安全锁芯）
由 UL（Underwriters Laboratories）测**锁对抗 8 种攻击的时钟时长**：pick 10 分钟、impressioning 10 分钟、钻/锯/撬/拉/冲 5 分钟等。

**一个重要的纠偏**（Lockwiki 明确指出）：**UL 437 并不定义美国的"高安全锁"标准**——它只是被 BHMA/ANSI A156.30 等高安全标准引用。很多厂商把 "UL 437 listed" 当营销词用，但它在法律/标准层面不是"高安全"的裁决者。

---

## 一个关键提醒：数字口径会打架

不同来源对 ANSI/BHMA 的 cycle 数字有差异（例如 Grade 1 锁具有来源写 800k、有来源写 1M）。原因包括：

1. **测试标准的版本更新**（A156.x 系列在迭代）；
2. **锁具类型不同**（mortise vs tubular latch vs deadbolt 的 cycle 阈值不同）；
3. **"锁具 cycle" vs "deadbolt cycle" 是两套数字**。

**结论**：读标准时，认"等级框架 + 测试维度"，不要死记某个具体数字。真正采购时，以具体型号的 BHMA Certified 产品目录 + 测试报告为准。

---

## The Author's Take

**我的判断：普通人选锁时最该建立的，不是"背出每套标准的数字"，而是"分清每套标准到底在测什么"。** 三点：

1. **ANSI Grade 测的是"耐用抗破坏"，不是"抗撬"**——一个 Grade 1 商用锁抗暴力很牛，但它的抗撬能力要看具体有没有 security pins / restricted keyway，Grade 本身不保证抗撬。
2. **EN 1303 的 8 位码 = 锁芯的"体检报告"**——与其纠结"这是不是好锁"，不如学会读那 8 位数字（尤其 Digit 7 钥匙安全、Digit 8 攻击抵抗）。这是欧洲体系最大的实用价值。
3. **"UL 437 listed" 是营销重灾区**——它测的是攻击抵抗时长，且不定义"高安全"。别看到 "UL 437" 就自动等于"顶级安全"。

结论：**别跨体系比大小（拿 Grade 比星级没意义），要在一个体系内逐项读。** 你要防的是"撬/钻/折"里的哪一种，就去读对应标准里那个维度的表现。

（以上是基于各标准公开说明 + Lockwiki/ScienceDirect 权威解读的专业判断，非第三方实测认证。）

---

## FAQ

**ANSI Grade 和 EN 1303 能直接比吗？**
不能。ANSI Grade 测耐用/抗破坏，EN 1303 是 8 位码逐维度。两套体系口径不同。

**UL 437 是"高安全锁"标准吗？**
严格说不是。它测攻击抵抗时长，不定义美国"高安全锁"，只是被其他高安全标准引用。

**TS007 和 EN 1303 什么关系？**
TS007 是英国星级标准，补 EN 1303 不测 snap（锁芯折断）的盲区。两者互补。

**住宅选锁认什么？**
北美看 ANSI/BHMA Grade 2–3，欧洲看 EN 1303 码，英国看 TS007 星级。

---

## Sources

- BHMA — Product Grade Levels（Grade 1–3 定义、A156 系列）
- Lockwiki — EN 1303 / UL 437（8 位码逐位解读、UL 437 攻击时长表、"不定义高安全"纠偏）
- Super Arbor / PDQ / Iveise — ANSI/BHMA Grade 1/2/3 cycle/impact/load 阈值
- ScienceDirect — High Security Standard（UL 437 攻击时长、pick 10min）
- Medeco（官方）— 高安全锁芯与 UL 437
- Keyman Lock / UMAY / SDH — EN 1303 与 TS007 差距、8 位码

> 具体测试数值随标准版本和锁具类型变动；采购以 BHMA 认证目录 + 型号级测试报告为准。

---

## 关联

- → EN 1303 8-Digit Code Decoded（Cluster）
- → ANSI/BHMA Grade 1/2/3 Decoded（Cluster）
- → 锁型机制（Pin Tumbler / Disc Detainer 等）
- → Entity：`#lock-standard` / `#ansi-bhma` / `#en-1303` / `#ul-437`
