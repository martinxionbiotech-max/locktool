---
title: "Fire-Rated Door Hardware Explained: NFPA 80, UL 10C, and Why \"Fire Exit\" ≠ \"Panic\" Hardware"
description: "Fire-rated door hardware explained: NFPA 80 self-closing/self-latching rules, UL 10C vs UL 10B positive-pressure testing, and why fire exit hardware is not panic hardware."
---
# Fire-Rated Door Hardware Explained: NFPA 80, UL 10C, and Why "Fire Exit" ≠ "Panic" Hardware

> 项目：Locktool · Content
> 类型：Standards Cluster（模板 G）
> 所属 Hub：Standards & Compliance Hub（/standards/）
> 主实体：`https://locktool.com/entity/nfpa-80#entity`、`https://locktool.com/entity/fire-door#entity`、`https://locktool.com/entity/fire-exit-hardware#entity`
> 状态：DRAFT（v0.2 工程参数升级）
> 研究日期：2026-09-12

---

## Quick Answer

防火门（fire-rated door）硬件的安全**不来自锁有多结实，而来自"门能不能在火灾时自己关紧并锁上"**。它必须通过**认证（listed + labeled）**，并满足 **NFPA 80 的两条硬要求——Self-Closing（自动关闭）+ Self-Latching（自动正锁舌）**。同时，门的防火评级由 **UL 10C（正压火灾测试）或 NFPA 252** 决定，而非任何锁的等级。

一句话：**防火门的价值在"合规"，不在"锁的等级"。**

---

## Definition

**Fire-rated door hardware**（防火门五金）：安装在防火门上的、经认证用于防火门组件（listed + labeled）的硬件，包括铰链、门闭器（closer）、锁具、逃生设备、flush bolt 等。其核心职能是确保门在火灾中**自动关闭并正锁舌（positive latching）**，从而维持防火分隔（compartmentalization）。

**两大核心标准**：

| 标准 | 发布主体 | 管什么 |
|---|---|---|
| **NFPA 80**（Standard for Fire Doors and Other Opening Protectives） | NFPA（美国消防协会） | 防火门的**安装、检查、维护、硬件要求** |
| **UL 10C / NFPA 252** | UL / NFPA | 门组件的**火灾测试方法**（决定防火评级分钟数） |

---

## 最关键的区分：Panic Hardware ≠ Fire Exit Hardware

这是消防检查里**最常见的错误认知**：

| 维度 | Panic Hardware（逃生推杆） | Fire Exit Hardware（防火逃生） |
|---|---|---|
| 目的 | 快速逃生（人多时推门而出） | 防火 + 逃生 |
| 适用 | 依 occupancy / 人流量决定 | 防火门强制 |
| **Mechanical Dogging** | ✅ 允许（可卡住保持常开） | ❌ **禁止** |
| 认证 | 逃生设备认证（A156.3） | 必须 **listed + labeled 用于防火门** |
| 释放力 | ≤ 15 lbf（A156.3） | 同逃生设备，但叠防火 listing |

**关键红线**：fire exit hardware **不允许 mechanical dogging**（把推杆卡住、让门保持常开）——因为防火门必须能**自动关闭 + 锁定**。用普通 panic hardware（带 dogging）装在防火门上，是典型检查失败。`[F]`

---

## 为什么 "Self-Closing + Self-Latching" 是命门

NFPA 80 要求防火门 self-closing + self-latching。背后的逻辑：

- 火灾时，门关上才能挡住火和烟；
- 门不光要"关上"，还要"锁舌伸进 strike 正锁舌（positive latching）锁住"，否则正压/烟一推就开。

**因此下列都是违规**（权威来源明确列出，`[F]`）：

1. **Roller latch（滚轮锁舌）**、**磁性碰扣**、**球扣** → 不符合 positive latching，防火门禁用。
2. **Mechanical dogging** → 让锁舌不伸，违反 self-latching。
3. **拆除/停用 door closer** → 违反 self-closing。
4. **用楔子/门挡/链条撑开门** → 禁止（除非用认证的电磁 hold-open 装置 + 消防联动释放）。

**工程细节**：防火门的门缝也有量化上限——底部 ≤ **3/4 英寸（19 mm）**、其余边 ≤ **1/8 英寸（3.2 mm）**（NFPA 80 §4.8.4 / §6.3.1.7 口径）。锁舌伸出（latch throw）由门的 listing 规定（典型 1/2–3/4 英寸），并标注在防火门标签上。`[F]`

---

## 硬件认证：label 是命根子

NFPA 80 要求防火门上**每一个组件**（铰链、closer、锁具、exit device、flush bolt）都必须是 **listed + labeled 用于防火门**：

- **替换非 listed 硬件 = 直接 void 防火评级**。
- **消防标签（fire label）被涂漆/损坏 = 评级作废**，需原厂或认证机构重新贴标，或整门更换。
- **现场钻孔/切割/改动 = 未授权改动，同样 void 评级**。

防火门标签需含：制造商名称、第三方认证机构标识、防火评级、火灾测试标准代号，以及（若 30 分钟温升 < 650°F / 343°C 时）温升信息。`[F]`

一句话：**防火门的评级，由"全套认证硬件 + 完好标签 + 无现场改动"共同维持，缺一即失效。**

---

## UL 10B vs UL 10C：为什么"正压测试"是关键

这是防火门评级里**最容易被忽略的工程区别**：

| 维度 | UL 10B（旧） | UL 10C（现行） |
|---|---|---|
| 全称 | Fire Tests of Door Assemblies | Positive Pressure Fire Tests of Door Assemblies |
| 压力条件 | 中性/负压（neutral/negative pressure） | **正压**（positive pressure，测试前 5 分钟后施加） |
| 中性压力面 | — | 距试样底部 **40 英寸** |
| 严格度 | 较低（有缝隙也可能通过） | 更高（真实火灾下热气/烟被压向未火面） |
| 现行用途 | 部分旧 listing / 特定场景 | **新防火门 listing 的主流标准** |

**关键认知**（`[F]`）：
- 真实火灾中，火面墙体处于**正压**，热气会从任何缝隙向外推。UL 10B 的中性压力炉让门"有缝也能过"，UL 10C 的正压则迫使门组件同时抗热 + 抗压。
- **IBC（国际建筑规范）要求 side-hinged 防火门用正压测试**，接受 UL 10C 或 NFPA 252 两种方法；UL 10C 已基本取代 UL 10B 用于新 listing。
- NFPA 252 是替代火灾测试方法，可做中性压或正压。

> 商业含义：买防火门时，"UL 10C listed" 比 "UL 10B listed" 更严格、更贴近真实火灾；老项目升级时也要确认 listing 用的是哪个标准。`[F]`

---

## The Author's Take

**Position**：我的判断是——防火门硬件是锁匠/门五金行业里"合规风险最高、最容易翻车"的领域之一，因为它赌的不是技术，而是人命安全；而翻车点几乎都出在"把逃生硬件当防火硬件用"和"现场乱改"这两件事上。

**Reasoning**：
1. **别把 panic 和 fire exit 当一回事**——这是检查员最常抓的错。带 dogging 的普通逃生推杆装防火门，等于亲手拆掉防火门的防火功能。装门时务必确认手上是 listed for fire door 的 fire exit hardware。
2. **"positive latching"是底线，别用滚轮/磁扣糊弄**——很多人为省钱或图方便用 roller latch，但这不满足 NFPA 80 的正锁舌要求。防火门必须用 listed cylindrical/mortise 锁具或 fire exit hardware。
3. **现场改动 = void 评级，正压测试 = 不能只看"防火分钟数"**——防火门不是普通门，不能随便钻孔、切边、换非认证零件；而且评级要看是 UL 10C（正压）还是 UL 10B（中性压），后者在真实火灾下可能漏烟漏火。

**Disclosure**：以上是基于 NFPA 80 公开要求 + 门五金行业资料的专业判断，非官方法规意见；具体执法以当地 AHJ（authority having jurisdiction）为准。

---

## FAQ

**Panic hardware 和 fire exit hardware 一样吗？**
不一样。fire exit hardware 是经认证用于防火门、且不允许 mechanical dogging 的逃生硬件。

**防火门能用 roller latch 吗？**
不能。NFPA 80 要求 positive latching（正锁舌），滚轮锁舌/磁扣/球扣都不符合。

**UL 10B 和 UL 10C 差在哪？**
UL 10C 是正压火灾测试（前 5 分钟后施加正压），更贴近真实火灾；UL 10B 是中性/负压。IBC 要求正压测试。

**防火门要多久检查一次？**
多数辖区要求 annual（每年）检查，查 label、closing、latching、门缝、无现场改动。

---

## Sources

- **NFPA 80**（Standard for Fire Doors and Other Opening Protectives）— NFPA；权威解读见 CDF Distributors（self-closing/self-latching、positive latch、label）与 US Made Supply（门缝 3/4"/1/8"、annual 检查、listing），访问 2026-09-12
- **UL 10C**（Positive Pressure Fire Tests of Door Assemblies）— UL / [Intertek](https://www.intertek.com/building/standards/ul-10c)（中性压力面 40 英寸、正压测试程序），访问 2026-09-12
- **UL 10B vs UL 10C** — US Made Supply / Coverstyl（中性 vs 正压、IBC 要求正压），访问 2026-09-12
- **NFPA 101 / IBC** — UpCodes Fire Door Hardware and Closures（latch required、自动关闭），访问 2026-09-12
- **ANSI/BHMA A156.3**（Exit Devices）— CDF Distributors（15 lbf 释放力、panic vs fire exit），访问 2026-09-12

---

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。凡属我方推断/折减的结论，已在「The Author's Take」中明确标注「专业判断」，不混同于来源事实。本文为信息性内容，非法律/法规意见。

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上来源均为标准组织/制造商/行业权威公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联

- → [Lock Security Standards Explained](lock-security-standards-explained.md)（Pillar，四体系对照）
- → [ANSI/BHMA Grade 1/2/3 Decoded](ansi-bhma-grades-decoded.md)（Grade 与防火门硬件的关系）
- → [EN 1303 Decoded](en-1303-decoded.md)（Digit 4 防火分级）
- → [Electronic Access Control Explained](../access-control/electronic-access-control-explained.md)（fire door 与 fail-safe 逃生关联）
- → [Electric Strike vs Maglock](../access-control/electric-strike-vs-maglock.md)（防火门电子锁的 fail-safe/fail-secure）
- → Entity：`https://locktool.com/entity/nfpa-80#entity` / `https://locktool.com/entity/fire-door#entity` / `https://locktool.com/entity/fire-exit-hardware#entity`
