# Key Cutting Machines Explained: Code vs Duplication, Edge vs High-Security Keys

> 项目：Locktool · Content
> 类型：Taxonomy Cluster（模板 A/B）
> 所属 Hub：Tools & Equipment Hub（/tools/）
> 主实体：`#key-cutting-machine`、`#key-blank`
> 状态：DRAFT
> 研究日期：2026-09-11

---

## Direct Answer

配钥机（Key Cutting Machine）分两大根本类型，对应两个完全不同的任务：

1. **Code Machine（码开机 / 原始切割机）**：从一串数字 bitting code，**没有实物钥匙**，直接切出一把原钥匙。
2. **Duplicator（复制机）**：追踪一把现有的钥匙，复制出一把副本。

另外还有一条**独立的维度**——切的钥匙是**边缘齿（edge style）**还是**高安全齿（high-security style）**，这决定你需要什么样的机器和刀具。

一句话：**丢失了但知道 code → 用码开机；手里有钥匙要备份 → 用复制机。** 两者几乎不能互相替代，专业锁匠通常至少需要两台机器。

---

## 维度一：Origination（码开）vs Duplication（复制）

### Origination（码开机）
从数字 code 切原钥匙，**不需要实物钥匙**。适合"钥匙全丢但锁有记录 code"的场景。

分三种：

| 类型 | 原理 | 特点 |
|---|---|---|
| **Manual（手动）** | 手动拨转刻度盘，逐位切深度 | 不需电脑、已有几十年历史、便宜 |
| **Automatic（电子自动）** | 软件控制自动切割 | 精准、省力、可处理复杂齿形 |
| **Punch（冲压）** | 冲压成型 | 适合批量同规格钥匙（如 master key 系统） |

### Duplication（复制机）
追踪现有钥匙复制。**快、简单，但必须有一把实物钥匙**。几乎所有标准钥匙坯都能复制。

**关键区别**：码开机切一把"原来的钥匙"很花时间，复制机则完全不能从 code 切——所以专业锁匠通常两台都要。

---

## 维度二：Edge Key vs High-Security Key

| 钥匙类型 | 代表 坯代号 / 型号 | 需要的机器 |
|---|---|---|
| **Edge Style（边缘齿）** | SC1、KW1、H75、Y11 | 标准配钥机（码开 + 复制均可） |
| **High-Security（高安全齿）** | HO01、LEX90、B119 | 需支持高安全齿形的机器 |

高安全钥匙通常有**侧铣（side milled）**或**激光切割（laser）**的齿形，需要机器支持对应的刀型和走刀路径。

---

## 钥匙坯（Key Blank）：配钥的前置步骤

配钥的第一步不是切，而是**选对钥匙坯**。Key blank 是未切割的钥匙金属体，它的：

- **keyway（钥匙道轮廓）**：两侧沟槽纹路，决定它能否插进某把锁；
- **肩（shoulder）/ 叶片（blade）/ 柄（bow）**：都标准化。

常见住宅坯：Kwikset（KW1）、Schlage（SC1）、Yale（Y1）、Weiser（WR5）。

**选坯原则**：切割前先试插空坯，确认能顺畅插入锁芯——插不进去或发紧，说明选错了 keyway。这一步能省下大量浪费和时间。

---

## The Author's Take

**我的判断：配钥这件事，新手最容易卡的不是"不会切"，而是"没分清码开和复制、以及没选对钥匙坯"。** 三点：

1. **码开和复制是两个业务，不是一台"全能机"能都干好的**——码开机切原钥匙极慢，复制机又不能从 code 切。指望一台机器通吃，通常两头都别扭。
2. **高安全钥匙是另一套体系**——如果你要服务汽车、商用高安全锁，得额外投入支持侧铣/激光齿形的机器，这是预算里的一个大项。
3. **选坯比切更基础**——坯选错，切得再准也是废钥匙。先学会读 keyway、选对坯，再谈切割精度。

（以上是基于锁匠配钥行业规范 + 配钥机分类常识的专业判断，非我方实测。）

---

## FAQ

**码开机和复制机有什么区别？**
码开机从数字 code 无实物切原钥匙；复制机追踪现有钥匙复制。两者任务不同，专业锁匠通常都要。

**钥匙坯是什么？**
未切割的钥匙金属体，带特定 keyway 轮廓。选对坯是配钥的前置关键步骤。

**高安全钥匙需要特殊配钥机吗？**
需要。侧铣/激光齿形需机器支持对应刀型和走刀路径。

---

## Sources

- CLK Supplies — Key Machine Guide（origination vs duplication、edge vs high-security、manual/automatic/punch）
- Lockpicks.com — Code Key Cutting Machines（"码开无实物、duplicator 追踪复制"）
- Lockpicks.com — How to Identify the Right Key Blank（钥匙坯、KW1/SC1/Y1/WR5、试插测试）
- Guardian Safe & Locks（视频）— Different Types of Key Cutting Machines

---

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。凡属我方推断/折减的结论，已在「The Author's Take」中明确标注「非实测/专业判断」，不混同于来源事实。

## 关联

- → Locksmith Tool Taxonomy（Pillar）
- → Lock Pick Types Explained
- → Entity：`#key-cutting-machine` / `#key-blank`
