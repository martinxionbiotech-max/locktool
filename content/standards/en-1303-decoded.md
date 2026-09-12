---
title: "EN 1303 Decoded: How to Read the 8-Digit Code on a Euro Cylinder Lock"
description: "EN 1303 decoded: read the 8-digit euro cylinder code digit by digit — durability, key security (1–6), attack resistance (0–D), corrosion and fire grades, with thresholds."
---
# EN 1303 Decoded: How to Read the 8-Digit Code on a Euro Cylinder Lock

> 项目：Locktool · Content
> 类型：Standards Cluster（模板 B/E）
> 所属 Hub：Standards & Compliance Hub（/standards/）
> 主实体：`https://locktool.com/entity/en-1303#entity`、`https://locktool.com/entity/euro-cylinder#entity`
> 状态：DRAFT（v0.2 工程参数升级）
> 研究日期：2026-09-12

---

## Quick Answer

EN 1303 是欧洲锁芯标准（现行 EN 1303:2015，英国采纳为 BS EN 1303:2015），用一个**8 位数字编码**概括 Euro cylinder 锁芯在 8 个维度上的表现。**学会读这 8 位数字，就等于拿到一把锁芯的"逐项体检报告"——尤其是 Digit 7（钥匙安全 1–6 级）和 Digit 8（攻击抵抗 0–D 级），能直接对比不同锁芯的真实差异。**

一句话：**与其问"这把锁芯好不好"，不如问"它的 EN 1303 码是多少、Digit 7 和 Digit 8 分别是什么 grade"。**

---

## Definition

**EN 1303**（Cylinders for locks，锁具用锁芯）：由欧洲标准化委员会（CEN）发布的标准，规定锁芯在**耐久、防火、耐腐蚀/温度、钥匙相关安全、攻击抵抗**等维度的**测试方法与分级阈值**。评估结果用一个 8 位数字码表示，每位数字对应一个维度，使不同锁芯可以逐项对比。现行版本为 **EN 1303:2015**。

> 例：一个典型编码 `1 6 0 B 0 C 5 D` 读作——使用类别 1、耐久 6（100,000 cycles）、门质量 0、防火 B、安全 0、腐蚀/温度 C、钥匙安全 5、攻击抵抗 D。`[F]`

---

## 8 位数字逐位解读

| 位数 | 维度 | 分级范围 | 一句话 |
|---|---|---|---|
| **Digit 1** | Category of Use（使用类别） | grade 1（唯一档） | 钥匙需承受 2.5 Nm 扭矩仍可用 |
| **Digit 2** | Durability（耐久） | grade 4 / 5 / 6 | 循环寿命 25k / 50k / 100k cycles |
| **Digit 3** | Door Mass（门质量） | grade 0（无要求） | 通常为 0 |
| **Digit 4** | Fire Resistance（防火） | grade 0 / A / B | 能否用于防火/防烟门 |
| **Digit 5** | Safety（安全性） | grade 0（无要求） | 通常为 0 |
| **Digit 6** | Corrosion & Temperature（腐蚀/温度） | grade 0 / A / B / C | 抗腐蚀 + 工作温度范围 |
| **Digit 7** | Key Security（钥匙安全） | **grade 1–6（6 最高）** | 防非法复制钥匙（key control） |
| **Digit 8** | Attack Resistance（攻击抵抗） | **grade 0–D（D 最高）** | 抗钻/凿/扭/拔芯的物理攻击 |

**工程洞察**：Digit 1、3、5 在实际中几乎恒为 `1` / `0` / `0`，**真正有区分度的是 Digit 2（耐久）、4（防火）、6（腐蚀）、7（钥匙安全）、8（攻击抵抗）**。读码时重点盯这五位。

---

## Digit 2 — 耐久（grade 4 / 5 / 6）

| Grade | 循环寿命 | 典型适用 |
|---|---|---|
| 4 | 25,000 cycles | 低频住宅/内部门 |
| 5 | 50,000 cycles | 常规住宅/轻型商用 |
| 6 | 100,000 cycles | 高流量/商用/公共 |

> 注意：耐久 grade 从 4 起跳（不是 1–3），这是 EN 1303 编码的一个易错点。`[F]`

---

## Digit 4 — 防火（grade 0 / A / B）

| Grade | 含义 | 测试/判定 |
|---|---|---|
| 0 | 不可用于防火/防烟门 | — |
| A | 防烟（smoke） | 按 EN 1634-3 做烟测试，或防烟部件熔点 ≥ 840°C |
| B | 防火（fire） | 按 EN 1634-1 / EN 1634-2 做火测试，或防火部件熔点 ≥ 300°C |

> 采购提示：装防火门的锁芯，Digit 4 至少要 A（防烟）或 B（防火），否则等于自降防火评级。`[F]`

---

## Digit 6 — 腐蚀/温度（grade 0 / A / B / C）

| Grade | 抗腐蚀 | 温度要求 |
|---|---|---|
| 0 | 无要求 | 无要求 |
| A | 高抗腐蚀 | 无温度要求 |
| B | 无腐蚀要求 | -25°C 至 +65°C |
| C | 高抗腐蚀 | -25°C 至 +65°C |

测试完成后，锁芯必须在 **-25°C 和 +65°C** 下用 **最大 1.5 Nm** 扭矩正常开锁。`[F]`

> ⚠️ 易错点：**Digit 6 是 grade 0/A/B/C（四档）**，**Digit 8 是 grade 0–D（五档）**。两者字母范围不同，读码时别张冠李戴。

---

## Digit 7 — 钥匙安全（grade 1–6，6 最高）

衡量**防非法复制钥匙 / key control** 的能力。分级的**工程参数**如下（`[F]`，源自 EN 1303:2015 的 Table 2 权威解读）：

| 参数 | grade 1 | grade 2 | grade 3 | grade 4 | grade 5 | grade 6 |
|---|---|---|---|---|---|---|
| 最小有效差数（effective differs） | 100 | 300 | 15,000 | 30,000 | 30,000 | 100,000 |
| 最小活动制栓数（movable detainers） | 2 | 3 | 5 | 5 | 6 | 6 |
| 最大相同台阶占比（identical steps） | 100% | 70% | 60% | 60% | 60% | 50% |
| 最大相邻相同台阶数 | — | 2 | 2 | 2 | 2 | 2 |
| 钥匙直接编码（direct coding on key） | — | — | 否 | 否 | 否 | 否 |
| 安全机制操作扭矩（interpassing） | 1.5 Nm | 1.5 Nm | 1.5 Nm | 1.5 Nm | 1.5 Nm | 1.5 Nm |
| 锁芯抗扭（torque resistance） | 2.5 Nm | 5 Nm | 15 Nm | 15 Nm | 15 Nm | 15 Nm |

**怎么读这张表**：grade 越高，锁芯的"有效钥匙差数"越多、活动制栓越多、抗扭越强，越难随便配出一把能开的钥匙。**grade 3 是一个关键分水岭**——从 grade 3 起"禁止钥匙直接编码"（钥匙上不能再直接刻出组合），这直接关系 key control（钥匙管控）与受限钥匙系统（restricted keyway）。

> 商业含义：物业/公寓/机构要防止钥匙被随意配，**至少选 Digit 7 = 4 及以上**，配合 restricted keyway（受限钥匙剖面）才能真正控钥匙。`[F]`

---

## Digit 8 — 攻击抵抗（grade 0–D，D 最高）

衡量**抗钻、抗凿、抗扭、抗拔芯**的物理攻击能力。分级工程参数如下（`[F]`，源自 EN 1303:2015 Table 3 权威解读）：

| 参数 | grade 0 | A | B | C | D |
|---|---|---|---|---|---|
| 抗钻（net drilling time） | — | 3–5 分钟 | 5–10 分钟 | 3–5 分钟 | 5–10 分钟 |
| 抗凿（chisel 击数） | — | 40 | 40 | 30 | 40 |
| 抗扭（twisting 次数） | — | 20 | 30 | 20 | 30 |
| 抗拔芯（extraction 力） | — | — | — | 10 kN | 15 kN |
| 抗拔芯（extraction 时长） | — | — | — | 5–15 分钟 | 5–15 分钟 |
| 锁芯抗扭（torque resistance） | — | 20 Nm | 30 Nm | 20 Nm | 30 Nm |

**怎么读这张表**：grade 0 无攻击抵抗要求；A/B/C/D 逐级覆盖更多攻击类型、更高阈值。**C 和 D 是"抗拔芯 + 抗钻凿扭"的完整档**，D 在抗钻时长（5–10 分钟）和抗拔芯力（15 kN）上最高。

> 商业含义：如果你的威胁是"有人用电钻钻锁芯"，**Digit 8 至少 A 级起**；高安全场景（商铺门、机构）考虑 C/D。注意 grade C 和 grade D 的抗钻时长区间相同（都是上限 10 分钟），差异在抗拔芯力（10 vs 15 kN）——**别只看"D 最高"就盲目上 D，要看具体威胁**。`[F]`

---

## EN 1303 的盲区：不测 Lock Snapping

EN 1303 有一个著名盲区——**不测 lock snapping（锁芯折断攻击）**。而 snap 恰恰是英国 Euro cylinder（尤其 uPVC/复合门）最常见的攻击方式：暴力掰断锁芯中心螺丝孔位置，然后伸手转动 cam 开门。

这就是英国推出 **TS007** 星级标准补洞的原因：

- **3 星锁芯**：单独抗 snap、pick、bump、drill、plug extraction。
- **1 星锁芯 + 2 星把手**：组合达到 3 星等效。
- 3 星测试引用 BS 3621、BS EN 1303、PAS 24 的要求。`[F]`

**结论**：EN 1303 看耐久/钥匙安全/攻击抵抗，但**在英国（或 uPVC 门环境），必须叠看 TS007 星级**——一个 EN 1303 攻击抵抗 D 级的高锁芯，照样可能被 snap 折断。

---

## The Author's Take

**Position**：我的判断是——EN 1303 是欧洲锁芯里最有用的"可逐项对比"工具，但它被太多人用成"一个笼统的等级标签"，反而丢了它的设计初衷。读码，比记"这锁是不是 EN 1303"重要一百倍。

**Reasoning**：
1. **读码 > 记等级**——8 位码的价值在"逐维对比"。两把锁芯，一把 Digit 7 = 6、一把 = 4，前者 key control 明显更强。只问"几级"，等于浪费这个标准。
2. **Digit 7 和 Digit 8 是两回事**——一个是"防复制钥匙"（key control），一个是"抗物理攻击"（anti-drill）。你的威胁是"钥匙被偷去配"还是"被钻/撬"，决定你盯哪一位。
3. **别忽略 snap 盲区，也别忘了 grade C/D 的微妙差异**——EN 1303 高攻击等级 ≠ 抗 snap（那要 TS007）；grade D 比 C 强的不是抗钻时长而是抗拔芯力（15 vs 10 kN），盲目追 D 可能多花钱却没解决你的真实威胁。

**Disclosure**：以上是基于 Lockwiki 对 EN 1303:2015 的逐位解读 + 欧标锁芯行业共识的专业判断，非认证机构结论，也不构成采购合规意见。

---

## FAQ

**EN 1303 的 8 位数字分别代表什么？**
使用类别、耐久、门质量、防火、安全、腐蚀/温度、钥匙安全、攻击抵抗。

**EN 1303 测 lock snapping 吗？**
不测。snap（锁芯折断）由英国的 TS007 星级标准覆盖。

**Digit 7 和 Digit 8 有什么区别？**
Digit 7 是钥匙安全（防复制，1–6 级），Digit 8 是攻击抵抗（抗钻/凿/扭/拔芯，0/A/B/C/D）。

**Digit 2（耐久）为什么是 grade 4–6 而不是 1–3？**
EN 1303 耐久分级从 grade 4 起跳（25k/50k/100k cycles），这是编码惯例，别和 Grade 1–3 的 ANSI 体系混淆。

---

## Sources

- **EN 1303:2015 / BS EN 1303:2015** — CEN / BSI；权威逐位解读见 [Lockwiki — EN 1303](https://www.lockwiki.com/index.php/EN_1303)（Digit 1–8 完整阈值表，引用 Eurospec Guide to BS EN 1303:2015），访问 2026-09-12
- Eurospec / Carlisle Brass — Guide to BS EN 1303:2015（8 位码示例 `1 6 0 B 0 C 5 D`、耐久 grade 4/5/6 循环数），访问 2026-09-12
- Master Key Systems — Euro Cylinder Locks Explained（TS007 1/2/3 星、snap 盲区），访问 2026-09-12
- Locksmiths.co.uk — Lock Snapping guide（3 星引用 BS 3621 / BS EN 1303 / PAS 24），访问 2026-09-12

---

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。凡属我方推断/折减的结论，已在「The Author's Take」中明确标注「专业判断」，不混同于来源事实。

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上来源均为标准组织/权威解读/制造商公开资料，非我方实测；关键数据已按来源等级区分 `[F]`（事实）/`[D]`（推导）。法规类信息随监管变化可能过期，执业前务必核实当地最新规定。

## 关联

- → [Lock Security Standards Explained](lock-security-standards-explained.md)（Pillar，四体系对照）
- → [ANSI/BHMA Grade 1/2/3 Decoded](ansi-bhma-grades-decoded.md)（北美体系对照）
- → [Dimple Lock Explained](../technology/dimple-lock-explained.md)（Euro cylinder 锁型与 snap 弱点）
- → [Fire-Rated Door Hardware Explained](fire-rated-door-hardware-explained.md)（Digit 4 防火在实际门上的落地）
- → Entity：`https://locktool.com/entity/en-1303#entity` / `https://locktool.com/entity/euro-cylinder#entity`
