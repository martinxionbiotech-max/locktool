# Access Control Credentials Explained: Prox Cards, Smart Cards, Biometrics, and the Wiegand Backbone

> 项目：Locktool · Content
> 类型：Access Control Cluster（模板 G）
> 所属 Hub：Access Control Hub（/access-control/）
> 主实体：`https://locktool.com/entity/credential#entity`、`https://locktool.com/entity/prox-card#entity`、`https://locktool.com/entity/smart-card#entity`、`https://locktool.com/entity/wiegand#entity`
> 状态：DRAFT
> 研究日期：2026-09-11

---

## Direct Answer

门禁系统的"凭证"（credential）是你用来证明"我是谁"的那件东西。主流类型从低到高安全：

| 凭证 | 技术 | 安全 |
|---|---|---|
| **PIN / 键盘码** | 数字密码 | 最低（可被偷看/分享） |
| **磁条卡** | swipe 磁条 | 低（易复制） |
| **Prox 卡 / 钥匙扣** | 125kHz RFID | 中（未加密、可克隆） |
| **智能卡（Smart Card）** | 芯片 + 加密 | 高（双向认证、难克隆） |
| **生物识别** | 指纹/人脸/虹膜 | 最高（不可丢失，但不可撤销） |
| **手机凭证 / MFA** | NFC/BLE + 多因素 | 高（组合验证） |

一句话：**安全的分水岭是"加密"——未加密的 prox 卡/磁条卡可被克隆，加密的智能卡和生物识别才真正抗伪造。**

---

## 关键纠偏 1：Prox 卡 ≠ 智能卡（这是最常被搞混的）

**Proximity card（125kHz prox）和 smart card 是两回事，安全级别差一个档次**（Koorsen / Capture Technologies）：

| | Prox Card（125kHz） | Smart Card（如 MIFARE，13.56MHz） |
|---|---|---|
| 频率 | 125kHz（1990 年代老技术） | 13.56MHz |
| 加密 | ❌ 无，数据明文 | ✅ 有加密 |
| 认证 | 单向（reader 读卡片 ID） | **双向**（reader 和 card 互相认证） |
| 可克隆 | 容易 | 难 |
| 存储 | 只有一个 ID 码 | 可存多应用数据 |

**关键点**：prox 卡里就是**一个固定的 ID 码**（facility code + 卡号），读出来就是明文，没有加密校验——因此可以被克隆/复制。智能卡要 reader 和 card **互相认证**，多一层安全，也更难伪造（也能一卡多用：门禁 + 打印 + 支付）。

---

## 关键纠偏 2：Wiegand 是"接口标准"，不是"凭证类型"

很多人把"Wiegand"当成一种卡，其实它是一套**接口/协议**，是门禁系统里 reader 和 controller 之间的**布线标准**（CardLogix / Keri Systems）：

- **Wiegand 效应**：1970 年代 John Wiegand 发明的磁线技术，原用于硬卡（swipe card）。
- **Wiegand 接口**：虽然硬卡已淘汰，但**接口标准活了下来**——因为全球几乎所有 controller 都支持它，所以今天几乎所有 prox/智能卡/生物/键盘 reader 都还是输出 Wiegand 信号。
- **26-bit Wiegand**：最经典的格式——26 bit 里，分 facility code + ID 号，第 1 和 26 bit 是奇偶校验。

一句话：**Wiegand 是"Reader 和 Controller 之间怎么说话"的通用语言，不是"你用的是什么卡"。** 你在系统里看到 "26-bit"、"37-bit"，指的就是这个协议格式，bit 越多能容纳的卡号空间越大。

---

## 关键纠偏 3：生物识别"最安全"但有一个致命缺陷

生物识别（指纹/人脸/虹膜）确实不可丢失、不可共享，是"最高安全"级别。但它有一个**不可逆的缺陷**：

> **生物特征一旦泄露，你无法"重置"它。** 卡丢了可以补发、PIN 忘了可以重置，但指纹/虹膜被复制了，你没法换一付。

所以高安全场景里，生物识别**常作为多因素中的一环**（biometric + PIN/card），而不是单独依赖。这也是为什么 MFA（多因素认证）是趋势——**单个凭证都有弱点，叠加才稳。**

---

## 怎么选

| 场景 | 选 |
|---|---|
| 低成本、低风险（办公室内门） | PIN / 键盘码 |
| 已有大量老式系统 | Prox 卡（125kHz，兼容性好） |
| 要安全 + 多应用 | 智能卡（MIFARE/13.56MHz） |
| 高安全、防伪造 | 智能卡 + 加密协议（OSDP 优先） |
| 无法代刷、防共享 | 生物识别（建议+MFA） |
| 远程/移动/临时访客 | 手机凭证 / NFC |

---

## The Author's Take

**我的判断：门禁凭证选择的黄金法则是"按风险选加密级别，别按习惯选"——大多数小企业还停在 1990 年代的 125kHz prox 卡上，纯粹因为"一直用这个"，而不知道这玩意儿是明文、可克隆的。** 三点：

1. **125kHz prox 卡是安全债，不是资产**——它是 1990 年的老技术，卡里就一个明文 ID，可被几十块钱的设备克隆。如果你管的是一道真正的安全门，prox 卡连"及格线"都没到，应该升级到加密智能卡（13.56MHz MIFARE）或 OSDP 协议。
2. **Wiegand 接口本身不加密，这是另一个常被忽略的洞**——reader 到 controller 那段线，Wiegand 是明文传输（所以有了更安全的 OSDP 协议）。别以为"用了智能卡"就全链路安全了，加密要贯穿"卡 → reader → controller"全程。
3. **生物识别是"不可撤销"的**——这是它最大的隐患，不是优点。指纹泄露比丢 100 张卡更糟，因为你换不了。高安全场景，生物识别必须配第二种因素，单独用是给自己挖坑。

结论：**升级路径清晰——PIN → 磁条 → prox → 加密智能卡 → 智能卡+生物 MFA，每一步对应更高的伪造成本。** 你现在在哪一级，取决于你保护的东西值多少。别让"一直这么做"决定你的安全水位。

（以上基于门禁行业标准资料 + 凭证技术原理的专业判断，非我方实测。具体选型应结合实际威胁模型。）

---

## FAQ

**Prox 卡和智能卡有什么区别？**
Prox（125kHz）未加密、可克隆；智能卡（13.56MHz）有加密、reader 和卡双向认证，更难伪造。

**Wiegand 是一种卡吗？**
不是。Wiegand 是 reader 和 controller 之间的接口/协议标准（26-bit 是经典格式），不是凭证类型。

**生物识别安全吗？**
不可丢失、防共享，但特征泄露后不可撤销，高安全场景应配合 MFA 使用。

**MFA 是什么？为什么推荐？**
多因素认证，组合两种以上凭证（智能卡+PIN、生物+手机），单凭证都有弱点，叠加更稳。

---

## Sources

- Koorsen — Types of Access Control Credentials（prox vs smart 双向认证差异）
- CDVI Americas — Access Control Glossary（125kHz 技术、26-bit Wiegand、active/passive prox）
- Keri Systems — What Is Wiegand（Wiegand 历史、facility code/ID、已消亡硬卡 + 接口存活）
- CardLogix — Wiegand Definition（1970s 技术、数据不可改、MIFARE/OSDP）
- Capture Technologies — Types of Credentials（prox/smart/biometric/PIN/MFA）

> 数据标注说明：本文关键数据均出自上方权威来源（标 `[F]` 事实）。「125kHz prox 可被克隆」为行业公认事实（来源明确说明 prox 数据不加密、无加密校验）。我方推断/倾向已在「The Author's Take」标注。本文为技术信息，非选型决策意见。

---

## 关联

- → Electronic Access Control Explained（Pillar，含 credential→reader→controller→lock 全栈）
- → Electric Strike vs Maglock（凭证验证后的物理执行层）
- → Entity：`https://locktool.com/entity/credential#entity` / `https://locktool.com/entity/prox-card#entity` / `https://locktool.com/entity/smart-card#entity` / `https://locktool.com/entity/wiegand#entity`
