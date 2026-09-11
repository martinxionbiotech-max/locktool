---
title: "Electronic Access Control Explained: Electric Strikes, Maglocks, and Fail-Safe vs Fail-Secure"
description: "Electronic access control explained: electric strikes, maglocks, and electrified locksets — plus why fail-safe vs fail-secure is the critical design decision."
---
# Electronic Access Control Explained: Electric Strikes, Maglocks, and Fail-Safe vs Fail-Secure

> 项目：Locktool · Content
> 类型：Taxonomy Pillar（模板 A/B）
> 所属 Hub：Access Control Hub（/access-control/）
> 主实体：`https://locktool.com/entity/electronic-lock#entity`、`https://locktool.com/entity/electric-strike#entity`、`https://locktool.com/entity/maglock#entity`
> 状态：DRAFT
> 研究日期：2026-09-11

---

## Direct Answer

电子门禁（Electronic Access Control）的核心，是把"锁"从"一把机械钥匙"升级成"一个由控制器决定的通电/断电信号"。它由几层组成：**凭证**（刷卡/手机/PIN/指纹）→ **读卡器** → **控制器/面板** → **电子锁硬件**。

最关键的硬件分三类，外加一个决定性的设计参数：

| 硬件 | 是什么 | 典型场景 |
|---|---|---|
| **Electric Strike（电控锁舌）** | 门框里的电动卡榫，通电释放门舌 | 金属/木门办公室门 |
| **Maglock（电磁锁）** | 靠电磁吸力抱住门 | 玻璃门、高流量门、自动门 |
| **Electrified Lockset（电动把手锁）** | 集成电子控制的把手锁/逃门 hardware | 需要机械手柄的商用门 |

**决定性参数——Fail-Safe vs Fail-Secure**：

- **Fail-Safe（断电开）**：断电时**解锁**——用于消防通道、逃生门，断电也必须能出去。
- **Fail-Secure（断电锁）**：断电时**保持锁**——用于高安全区，断电也不让进。

一句话：**选电子锁硬件，先问"断电时这扇门该开着（逃生）还是锁着（防盗）"，再选 fail-safe 或 fail-secure。** 这是电子门禁里最容易被忽略、却最要命的设计点。

---

## 三大硬件的区别

### Electric Strike（电控锁舌）
- 门框内的电动卡榫，由**电磁线圈**驱动一个小元件伸缩。
- **默认锁、通电开**（最常见），但可做成 fail-safe 或 fail-secure。
- **唯一能"fail-safe 或 fail-secure 二选一"的锁型**，适合高安全区（断电也要锁）。
- 不能装在**玻璃门**上。

### Maglock（电磁锁）
- 靠**电磁吸力**（常 600–1200 lb）把门抱在门框上。
- 本质是 **fail-safe 设备**——断电即失磁解锁（所以消防报警必须联动）。
- 适合**玻璃门、高流量门、自动门**，但断电默认开（不适合"断电也要锁"的场景）。

### Electrified Lockset / Panic Hardware（电动把手/逃生 hardware）
- 集成电子控制的机械把手锁、或电动 **panic（逃生推杆）**硬件。
- 用于需要"物理手柄 + 电子权限"的商用门。

---

## 一个关键工程细节：低压供电

商用电子锁走 **低电压（12V 或 24V DC）** 布线，连接到门控制器（controller）。控制器负责：

- 供电、状态监控、读卡器输入；
- **maglock 和 fail-safe 设备的消防报警联动**（通常用 relay 模块）——这是法规硬要求。

大型项目可用 **PoE 控制器**减少布线。无线锁则通过网关/中枢连到门禁软件（品牌如 Lenel、S2、Kisi、Openpath、Brivo、Verkada，常需 license/模块）。

---

## The Author's Take

**我的判断：电子门禁里,锁匠和系统集成商最容易翻车的点，就是 fail-safe vs fail-secure 的错配。这不是细节，是安全责任问题。** 三点：

1. **"断电时这扇门该开还是锁"是消防法规问题，不是技术偏好**——逃生门错配成 fail-secure（断电锁死），关键时刻会堵死逃生通道，是严重责任事故。
2. **maglock 是"天生 fail-safe"**——因为它靠电磁，断电必失磁解锁。想在高安全区用 maglock，必须接受"断电即开"的物理本质，靠其他手段（备用电源、门磁报警）补偿。
3. **electric strike 是"可二选一"的灵活性之王**——它既能 fail-safe 也能 fail-secure，是大多数"既要逃生合规、又要某些门防盗"项目里的默认选择。

结论：**做电子门禁项目，先画一张"每扇门断电时该开还是锁"的清单，再逐门选硬件。fail-safe/fail-secure 不是按钮，是安全和合规的底线设计。**

（以上是基于电子门禁公开标准 + Kisi/Avigilon/GenX 等从业者指南的专业判断，非我方实测。）

---

## FAQ

**Fail-safe 和 fail-secure 有什么区别？**
Fail-safe 断电时解锁（逃生门用），fail-secure 断电时保持锁（高安全区用）。

**Maglock 是 fail-safe 还是 fail-secure？**
天生 fail-safe——靠电磁吸力，断电即失磁解锁。消防报警必须联动。

**Electric strike 能装玻璃门吗？**
不能，主要装金属/木门。玻璃门用 maglock。

**电子门禁走什么电压？**
商用电子锁通常 12V 或 24V DC 低电压布线，连接门控制器。

---

## Sources

- Kisi — Electronic Locks Guide（electric strike/maglock、fail-safe/fail-secure、玻璃门限制）
- Avigilon — Electric vs Magnetic Strike Locks（electric strike 原理、应用场景对比）
- GenX Security — Electronic Door Locks 101（electrified handleset/strike/panic/maglock、12/24V、Lenel/S2/Kisi 等品牌）
- Silver Star Protection — Commercial Access Control Glossary（凭证/读卡器/控制器/硬件分层）
- ButterflyMX — 5 Types of Commercial Access Control（key fob/keypad/mobile/cloud/intercom）

---

## 关联

- → Lock Security Standards Explained（标准总览）
- → Automotive Key Programmers Explained（电子/芯片锁的另一维度）
- → Entity：`https://locktool.com/entity/electronic-lock#entity` / `https://locktool.com/entity/electric-strike#entity` / `https://locktool.com/entity/maglock#entity`
