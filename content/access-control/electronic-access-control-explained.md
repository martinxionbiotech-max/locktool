---
title: "Electronic Access Control Explained: The Credential-to-Lock Stack, Fail-Safe vs Fail-Secure, and the Code That Governs It"
description: "Electronic access control explained: the credential → reader → controller → lock → fire-interface stack, fail-safe vs fail-secure, and the NFPA 101 / UL 294 / ANSI/BHMA standards that govern egress hardware."
---
# Electronic Access Control Explained: The Credential-to-Lock Stack, Fail-Safe vs Fail-Secure, and the Code That Governs It

> 项目：Locktool · Content
> 类型：Taxonomy Pillar（模板 A/B）
> 所属 Hub：Access Control Hub（/access-control/）
> 主实体：`https://locktool.com/entity/electronic-lock#entity`、`https://locktool.com/entity/electric-strike#entity`、`https://locktool.com/entity/maglock#entity`、`https://locktool.com/entity/fail-safe#entity`、`https://locktool.com/entity/fail-secure#entity`
> 状态：UPGRADED v0.2
> 研究日期：2026-09-12

---

## Quick Answer

Electronic access control (EAC) replaces the mechanical key with a **powered signal** that a controller decides to send. It is a five-layer stack — **credential → reader → controller → electrified lock → power/fire interface** — and the one decision that overrides all others is **fail-safe vs fail-secure**: whether a given door unlocks or stays locked when power is cut.

> **Definition — Electronic Access Control:** a system in which an electrified locking device (electric strike, electromagnetic lock, or electrified lockset) is released by a controller after it validates a credential. The behavior of the door's *access (secure) side* when power fails is classed as **fail-safe** (unlocks) or **fail-secure** (stays locked).

## The Five-Layer Stack

Every EAC system, from a single office door to a campus, is the same five layers. Understanding which layer owns which failure mode is the whole game:

| Layer | What it does | Typical failure it owns |
|---|---|---|
| **1. Credential** | Proves "who" — card, phone, PIN, biometric | Weak credential = forged identity |
| **2. Reader** | Reads the credential, sends data to controller | Unencrypted reader-to-controller link (Wiegand) |
| **3. Controller / panel** | Validates credential, decides to release the lock, logs events | Panel decision logic, fire-alarm interface |
| **4. Electrified lock** | Electric strike / maglock / electrified lockset | Fail-safe vs fail-secure on power loss |
| **5. Power + fire interface** | Low-voltage supply, relay tie to fire alarm / sprinkler | Loss of power behavior, alarm release |

The layered view matters because **security is only as strong as the weakest link** — an encrypted credential on a plain-Wiegand wire, or a fail-secure strike on an egress door, undoes the other layers' work.

## Fail-Safe vs Fail-Secure: The Decision That Governs Everything

The terms describe the **access (secure / key / outside) side** of the door — not the egress side. Allegion's definition is the cleanest [F]:

- **Fail-safe** = *unlocked on the access side when power is removed; power is applied to lock.*
- **Fail-secure** = *locked on the access side when power is removed; power is applied to unlock.*

Three clarifications that prevent most mistakes:

1. **Both modes normally still permit free egress.** On most doors the occupant can always exit from inside (free egress); fail-safe/fail-secure describes the *outside* side. A fail-secure lock does **not** trap people — *unless* it's an institutional/restricted arrangement without a mechanical override.
2. **Maglocks are inherently fail-safe.** Electromagnetism releases the instant power drops; you cannot order a fail-secure maglock.
3. **Electric strikes are the flexible ones.** A given strike model is often field-selectable between the two — which is why confirming how a strike is actually wired matters (NGTECO/Axis [F]).

| | Fail-Safe | Fail-Secure |
|---|---|---|
| On power loss (access side) | **Unlocks** | **Stays locked** |
| Power's job | Applied to *lock* | Applied to *unlock* |
| Use | Egress/fire routes, stairwell re-entry | Server rooms, storage, perimeter |
| Hardware | Maglock (always), fail-safe strike/lockset | Fail-secure strike/lockset |
| Fire-door compatibility | Fail-safe strike **cannot** be used on a fire-rated opening | Fire-rated strikes are fail-secure only |

## The Three Locking Hardware Families

### Electric Strike (frame-mounted actuator)
- A keeper in the door **frame** that replaces the standard strike plate; an electromagnetic coil pivots a small latch lip to release the lock's bolt/latch.
- **Keeps the mechanical lock unchanged** — the lever/handle and latch still do the physical holding; the strike only controls whether the latch can be pulled past it.
- Configurable fail-safe **or** fail-secure; most deployments are **fail-secure** (Axis [F]).
- Governed by **ANSI/BHMA A156.31**; burglar-resistant variants are **UL 1034** listed.
- Cannot be used on frameless glass doors (no frame to cut the strike into).

### Maglock (electromagnetic lock)
- An electromagnet on the frame plus a steel **armature plate** on the door; holding force keeps the door shut.
- **Inherently fail-safe** — no power, no magnetism, no hold. This is a physical fact, not a setting.
- Governed by **ANSI/BHMA A156.23**.
- Ideal for glass/aluminum-frame doors and high-traffic openings where a mechanical strike can't be fitted; **requires** a REX (request-to-exit) device for egress compliance (see below).

### Electrified Lockset / Panic Hardware
- A mechanical lockset (mortise or cylindrical) or panic/exit device with an electrical actuator integrated, so the mechanical handle + electronic permission coexist.
- Keeps a **physical handle/lever** on the door — the most "code-friendly" option for doors that need both mechanical egress and electronic access control.

## Low-Voltage Power and the Fire Interface

Commercial EAC locks run on **low-voltage DC (typically 12 V or 24 V)**, supplied by a power supply or the controller, wired to a relay that the controller toggles. Two engineering facts that matter:

- **PoE controllers** (Power over Ethernet) reduce cabling on larger jobs; wireless locks use a gateway/hub to reach the access-control software.
- **Fire-alarm/sprinkler integration is mandatory, not optional** for fail-safe devices on egress doors: the fire-alarm relay must **drop power to the lock** on alarm, and the door must stay unlocked until the panel is reset (National Training Center [F]).

## The Code Layer: What Makes an Electronically Locked Door Legal to Egress

This is where installs pass or fail inspection. The relevant rules (NFPA 101 §7.2.1.6.2 "access-controlled egress doors"; IBC "sensor release of electromagnetically locked egress doors", formerly §1008.1.9.8) require, in combination:

1. **Sensor release** — a sensor detects an approaching occupant and unlocks the door in the direction of egress, with **no time delay**.
2. **Manual release backup** — a device labeled **"PUSH TO EXIT"**, mounted **40–48 inches** above the floor and **within 5 feet** of the door, that keeps the door unlocked for **a minimum of 30 seconds**.
3. **Fire-alarm / sprinkler release** — activation of the fire alarm or sprinkler system must unlock the door automatically, and it must remain unlocked until the panel is reset.
4. **Loss-of-power release** — the door unlocks on loss of power to the lock, the sensor, or the access-control system.
5. **UL 294 listing** — recent code editions require the access-control equipment to be **listed per UL 294** (IBC first referenced UL 294 in the 2012 edition).

**Delayed egress** (§7.2.1.6.1) is a *separate, more restrictive* arrangement: a door that unlocks only after a **15- or 30-second** delay, with **"PUSH UNTIL ALARM SOUNDS" / "DOOR CAN BE OPENED IN 15 (30) SECONDS"** signage, an audible signal, and **irreversible** release once initiated. It is allowed only in specific occupancies — not a default.

## Accessibility (ADA/ABA) and OSHA

- **ADA/ABA §404.2.9**: interior hinged doors (non-fire-rated) on accessible routes open with **≤5 lbf**. Exceptions: fire doors, exterior hinged doors, and the force to retract a latch bolt. **§404.2.7**: hardware must be operable **one-handed, no tight grasping/pinching/twisting, ≤5 lbf** — which effectively bans round knobs on accessible doors.
- **Closing speed**: a door closer must move the door from 90° to 12° open in **≥5 seconds**.
- **OSHA 29 CFR 1910.36(d)**: workplace exit-route doors must be **unlocked from the inside**, and must not have any device/alarm that could restrict emergency use if it fails.

The accessibility note with real teeth for EAC: **a fire-rated door that needs >5 lbf to open is not accessible by force alone** — the standard fix is an automatic/power-assist operator, not simply adjusting the closer.

## The Author's Take

**Position:** In my view, most electronic-access-control failures are *specification* failures, not hardware failures — and the two places they happen are the fail-safe/fail-secure call and the reader-to-controller link.

**Reasoning:** First, fail-safe vs fail-secure is a life-safety decision that must be made door-by-door against the egress code, yet it's routinely treated as a "config toggle" buried in a spec. Second, people over-index on the credential's encryption while the Wiegand wire between reader and controller runs in plaintext — encryption has to span the whole stack to mean anything. Third, the code's insistence on REX + fire-alarm release + no-delay egress is exactly what separates a legal opening from an inspection failure, and it's the part buyers skip because it "looks optional."

**Disclosure:** This is my professional opinion grounded in the NFPA 101/IBC egress provisions, UL 294, and the ANSI/BHMA standards cited below — not first-party test data.

## FAQ

**Fail-safe and fail-secure — what's the difference?**
Fail-safe unlocks on the access side when power is removed (egress routes); fail-secure stays locked (high-security areas). Both normally still permit free egress from inside.

**Is a maglock fail-safe or fail-secure?**
Inherently fail-safe — electromagnetism releases the instant power drops. You cannot buy a fail-secure maglock.

**Can an electric strike go on a glass door?**
No — it needs a frame to cut the strike into. Glass/aluminum-frame doors use maglocks.

**What does UL 294 actually test?**
Four performance categories, each Level I–IV: destructive attack, line security, endurance, and standby power. Level I is the baseline that establishes egress safety.

**Why is a REX device mandatory on a maglock door?**
Because a maglock has no mechanical egress; code requires a sensor or "PUSH TO EXIT" device so occupants can leave without prior knowledge or special action.

## Sources

- Allegion / I Dig Hardware — "Decoded: Fail Safe vs. Fail Secure" (2023-10): https://idighardware.com/2023/10/decoded-fail-safe-vs-fail-secure-when-and-where — fail-safe/secure definitions referencing the secure side
- Allegion / I Dig Hardware — "Decoded: Code Requirements for UL 294" (2015-12): https://idighardware.com/2015/11/decoded-code-requirements-for-ul-294-standard-for-access-control-system-units-december-2015 — UL 294 four levels; IBC 2012 first reference
- Locksmith Ledger — "Understanding UL 294": https://www.locksmithledger.com/electronics-access-control/article/12264560/understanding-ul-294 — Level I establishes egress safety
- UL Solutions — "Securing Peace of Mind: Access Control and Gate Operators": https://www.ul.com/news/securing-peace-mind-access-control-and-gate-operators — UL 294 7th edition (2017-01-31), four performance levels
- NFPA — "Permissible Egress Door Locking Arrangements" (2021-07-09): https://www.nfpa.org/news-blogs-and-articles/blogs/2021/07/09/swinging-egress-door-operation-permissible-egress-door-locking-arrangements — sensor-release egress doors
- Consulting-Specifying Engineer — "Door locking requirements in NFPA 101": https://www.csemag.com/door-locking-requirements-in-nfpa-101 — manual release PUSH TO EXIT, 30 s, delayed egress 15/30 s
- National Training Center — "Access Control – Egress Requirements": https://nationaltrainingcenter.com/access-control-egress-requirements — PUSH TO EXIT 40–48 in / within 5 ft / ≥30 s; fire-alarm release
- U.S. Access Board — "Chapter 4: Entrances, Doors, and Gates": https://www.access-board.gov/ada/guides/chapter-4-entrances-doors-and-gates — §404.2.9 (5 lbf), §404.2.7 (hardware)
- Allegion — "Accessibility Solutions": https://us.allegion.com/en/solutions/by-requirement/accessibility-solutions.html — opening force, closing speed ≥5 s
- eCFR — 29 CFR 1910.36: https://www.ecfr.gov/current/title-29/subtitle-B/chapter-XVII/part-1910/subpart-E — OSHA exit-route door unlocked requirement
- Axis — "Fail-safe vs fail-secure: What's the difference": https://newsroom.axis.com/en-us/blog/fail-safe-vs-fail-secure — strikes mostly fail-secure; mechanical override on fail-secure doors
- BHMA — "A156.31-2024 Electric Strikes and Frame Mounted Actuators": http://buildershardware.com/ANSI-BHMA-Standards/Hardware-Highlights/A15631-2024-Electric-Strikes-and-Frame-Mounted-Actuators — Grade 1 cycle testing

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上均为第三方权威标准组织/制造商/监管公开资料，非我方实测；关键数据按来源等级标注 `[F]`（事实）/`[D]`（推导）。法规类信息随监管变化可能过期，执业前务必核实当地现行规定与 AHJ 执法口径。本文为技术科普与选型参考，非法律/法规意见。

## 关联

- → [Access Control Credentials Explained](access-control-credentials-explained.md)（栈的第 1–3 层：凭证/读卡器/Wiegand）
- → [Electric Strike vs Maglock](electric-strike-vs-maglock.md)（栈的第 4 层：锁具硬件对比）
- → [Fire-Rated Door Hardware Explained](../standards/fire-rated-door-hardware-explained.md)（NFPA 80 与逃生硬件，fail-safe 的消防关联）
- → [ANSI/BHMA Grades Decoded](../standards/ansi-bhma-grades-decoded.md)（A156.x 分级体系如何读）
- → [Safe Lock Types Explained](../vault/safe-lock-types-explained.md)（UL 768 电子保险柜锁，另一电子锁域）
- → Entity：`https://locktool.com/entity/electronic-lock#entity` / `https://locktool.com/entity/electric-strike#entity` / `https://locktool.com/entity/maglock#entity` / `https://locktool.com/entity/fail-safe#entity` / `https://locktool.com/entity/fail-secure#entity`
