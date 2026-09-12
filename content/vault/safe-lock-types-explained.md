---
title: "Safe Lock Types Explained: Mechanical Dial vs Key vs Time Lock vs Electronic vs Biometric (UL 768 Groups & EN 1300 Classes)"
description: "Safe lock types explained: mechanical dial, key, time lock, electronic keypad, and biometric — plus UL 768 Group 2/2M/1/1R, UL 2058 Type 1, and EN 1300 Class A/B/C/D decoded."
---
# Safe Lock Types Explained: Mechanical Dial vs Key vs Time Lock vs Electronic vs Biometric (UL 768 Groups & EN 1300 Classes)

> 项目：Locktool · Content
> 类型：Comparison Pillar（模板 A/C）
> 所属 Hub：Vault & Safe Hub（/vault/）
> 主实体：`https://locktool.com/entity/safe-lock#entity`、`https://locktool.com/entity/ul-768#entity`、`https://locktool.com/entity/en-1300#entity`
> 状态：DRAFT
> 研究日期：2026-09-12

---

## Quick Answer

Safe locks fall into **five families** distinguished by what drives the bolt and what can fail:

| Family | Actuation | Primary failure mode | Best for |
|---|---|---|---|
| **Mechanical dial (combination)** | Wheels + gates + fence aligned by dialing | Mis-dialing, worn wheels, lost combination | Long-term, no-power reliability |
| **Mechanical key lock** | Double-bitted key rotates a bolt/lever pack | Lost key, key duplication, keyway wear | Secondary lock, simple cabinets |
| **Time lock / time-delay** | Clockwork or timer gates opening | Clock drift, dead battery (electronic variants) | Banking, armed-robbery deterrence |
| **Electronic keypad** | Battery + PIN drives a solenoid/stepper | Battery, keypad circuit, ESD | Frequent access, multi-user, audit |
| **Biometric** | Fingerprint sensor releases bolt | Sensor wear, false reject, spoofing | Rapid single-user access |

The lock's **security rating** — not its family — is what matters for manipulation resistance. Mechanical locks are graded by **UL 768** (Group 2 → 2M → 1 → 1R) or **EN 1300** (Class A → B → C → D); electronic locks are graded by **UL 2058 Type 1** or **EN 1300**. The lock rating measures **resistance to non-destructive opening** (manipulation, radiological imaging, electronic attack) — it never tests the body, which is rated separately ([UL 1037 / UL 687](safe-burglary-ratings-decoded.md), EN 14450 / EN 1143-1).

> **Definition:** A **safe lock** is the locking component that blocks the safe's boltwork and releases it only upon a valid credential (dialed combination, key, PIN, or biometric). Its *security grade* (UL 768 Group, UL 2058 Type 1, or EN 1300 Class) is a tested measure of resistance to unauthorized opening by a skilled attacker using defined techniques and time budgets — independent of the safe body it is mounted in.

---

## Mechanical Dial Locks: How They Work and Why They Fail

A combination dial lock is pure mechanical engineering. Turning the dial drives a **drive cam** that rotates a stack of **tumbler wheels** (typically three or four). Each wheel carries a **gate** (a notch). When all gates align under the **fence**, the fence drops in, the **lever** engages, and the bolt retracts. There is no power source, no firmware, and no battery to die.

**Key engineering parameters that define the security grade:**

- **Dialing tolerance** — how many graduations off the true number still open the lock. Tighter tolerance = harder to manipulate. Group 2 allows ±1.25 graduations on a 3-wheel lock (±1.50 on 4-wheel); Group 1 tightens to ±1.00 (±1.25 on 4-wheel) `[F]`.
- **Combination space** — a UL 768 lock must allow at least **1,000,000 combinations** `[F]`. More wheels or a 4-wheel design multiplies this (≈10^8 for 4-wheel Group 2), but raw combination count is not the main defense — *manipulation resistance* is.
- **Relock trigger** — a spring-loaded secondary catch that fires if the lock is punched or the dial is driven, immobilizing the bolt. Group 1 locks are tested so that "punching" immobilizes the bolt mechanically `[F]`.

**Primary failure modes:** mis-dialing under stress, wheel wear over decades, a lost combination (typically requires a licensed professional to reset), and — the one many owners ignore — *the combination can be guessed if left at the factory default*.

**Representative locks:** Sargent & Greenleaf 6730 (Group 2 workhorse), La Gard 3300/3330 series, Big Red. European equivalents are certified to EN 1300.

---

## Mechanical Key Locks

A double-bitted key (or circular key) rotates a lever pack that throws the bolt. Key locks are fast and cheap, but their security rests entirely on **key control** — who can copy the key and whether the keyway is restricted. In UL terms, a **Type 1 key lock** is rated for ≥20 hours resistance to picking/impressioning plus 60 minutes against forcing, drilling, sawing, prying, pulling, and driving; a **Type 2** key lock for ≥30 minutes combined `[F]`.

**Primary failure modes:** lost keys, unauthorized duplication, keyway wear, and forcing the keyway. Key locks are most often used as the *secondary* lock on dual-lock high-grade safes, not as the primary defense.

---

## Time Locks and Time-Delay Locks (Not the Same Thing)

Two often-confused mechanisms:

- **Time lock** — unlocks only at a *preset clock time* (e.g., a bank vault cannot be opened before the next business day). Mechanical movements, typically **two-movement** for redundancy `[F]`.
- **Time-delay lock** — after a valid code is entered, the lock waits a programmable **1–99 minute** delay before releasing; used to deter armed robbery (a robber cannot force a fast open). Many add a **duress code** that starts the delay and silently alerts a monitoring centre `[F]`.

**Primary failure modes:** mechanical clock drift (time locks), and, in electronic variants, the delay timer's non-volatile memory is relied upon so a battery change does not reset the timer `[F]`.

---

## Electronic Keypad Locks

A battery-powered keypad accepts a PIN. On a correct entry, an electrical signal drives a **solenoid or stepper motor** to retract the bolt. The security standard is **UL 2058**, which has a **single grade — Type 1**; there is no "Type 2" high-security electronic tier `[F]`. A Type 1 lock is tested against expert manipulation, radiological attack, **electrostatic discharge (ESD)**, **voltage injection**, and **RF/electromagnetic attack**, plus endurance.

**Two facts that trip up buyers:**

1. **A UL Type 1 electronic lock has no key override by design.** UL will not certify a Type 1 lock that includes a physical key backup, because the keyhole reintroduces an attack surface `[F]`. If a keypad lock has a key override, it is *not* Type 1.
2. **The "million combinations" figure is not the point.** A Type 1 electronic lock may offer far more code combinations than a Group 2 mechanical lock, but brute-force code guessing is not a realistic attack; the tested ESD/RF/manipulation resistance is.

**Primary failure modes:** dead battery (most commonly the external keypad fails, not the lock body — the keypad can often be replaced without drilling, per Liberty Safe `[F]`), ESD damage, and the reliability cost quantified in the [mechanical-vs-electronic](mechanical-vs-electronic-safe-locks.md) page's "20:1 drilling ratio" industry observation.

**Representative locks:** SecuRam, La Gard, Sargent & Greenleaf Type 1 packages.

---

## Biometric Locks

A fingerprint (or occasionally other biometric) sensor authorizes the bolt. Biometric is best understood as an **electronic lock with a biometric credential** rather than a separate security category — its security grade still comes from the lock's electronic standard. The decision is dominated by **sensor quality**: false-reject rate (legitimate user denied), false-accept rate (wrong print accepted), and sensor longevity.

**Primary failure modes:** sensor wear, dirty/dry fingerprints causing false rejects, and spoofing of low-end sensors. For most residential use, biometric trades a marginal speed gain for a meaningful reliability and spoofing risk; verify the underlying electronic lock is genuinely UL Type 1 or EN 1300 certified rather than trusting the "biometric" label.

---

## The Two Rating Systems (This Is the Whole Point)

### North America: UL 768 Groups (mechanical) and UL 2058 Type 1 (electronic)

UL 768 provides **three** core ratings for combination locks — **Group 2, Group 1, Group 1R** — plus **Group 2M** `[F]`:

| Group | Manipulation resistance | Radiological (X-ray) resistance | Notes |
|---|---|---|---|
| **Group 2** | Moderate (no fixed hour budget) | — | Min 1,000,000 combos; ±1.25 (3-wheel) / ±1.50 (4-wheel) tolerance |
| **Group 2M** | **2 working hours** | — | The "M" is manipulation, *not* radiological |
| **Group 1** | **20 working hours** | — | Advanced anti-manipulation features; ±1.00 (3-wheel) / ±1.25 (4-wheel); punch-immobilizes |
| **Group 1R** | 20 working hours (all Group 1 reqs) | **20 hours** (≤10 curies cobalt-60 at 30") | Acetal resin wheels that don't image under X-ray; **the DEA's requirement** for Schedule I/II storage |

**Two corrections that matter:**

1. **Group 2M is *manipulation* resistance (2 hours), not radiological.** Radiological resistance is **Group 1R** (the "R"). Many retailer descriptions conflate the two `[F]`.
2. **Group 1R is the only mechanical grade the US DEA accepts** for safes storing Schedule I/II controlled substances — and **electronic locks do not meet that specific DEA requirement** even at Type 1, because DEA specifies a Group 1R mechanical lock paired with a TL-30 safe `[F]`.

### Europe: EN 1300 Classes (A/B/C/D)

EN 1300 (first published 2004) is the European classification for **high-security locks** used on safes, strongrooms, and ATMs certified to EN 14450 or EN 1143-1. It grades *any* lock type — key, mechanical combination, or electronic — into **four classes**:

| Class | Security level | Typical application |
|---|---|---|
| **A** | Lowest (of the four) | Basic safes, EN 14450 S1/S2, EN 1143-1 Grade 0–2 |
| **B** | Medium | Commercial safes, EN 1143-1 Grade 3–5 |
| **C** | High | Banking/financial, EN 1143-1 Grade 6–11 |
| **D** | Highest | Government, cash-in-transit, Grade 11–13 |

EN 1300 is **not only a security grade** — it also tests **reliability**: every lock must function normally after **10,000** open/close cycles, and a mechanical combination lock after **100** code changes `[F]`. Certification is issued by independent bodies — **ECBS (European Certification Body GmbH)** maintains the authoritative EN 1300 lock list, with VdS among the other accredited certifiers `[F]`.

**A subtle but important rule:** the lock's class depends on its *input device*. For example, the La Gard 1947 combination lock is only Class C when fitted with the spy-proof 1730/1731 dial — the dial (input device) is part of the certified system, and swapping it can change the class `[F]`.

### Which lock class does each safe grade require?

EN 1143-1 and EN 14450 *prescribe* the lock class — the body grade and lock class are coupled in the European system:

| Safe/cabinet grade | Required lock (EN 1300 / EN 17646) |
|---|---|
| EN 14450 S1, S2 | 1 × Class A |
| EN 1143-1 Grade 0–2 | 1 × Class A |
| Grade 3 | 1 × Class B |
| Grade 4–5 | 2 × Class B |
| Grade 6–10 | 2 × Class C |
| Grade 11–12 | 3 × Class C or 2 × Class D |
| Grade 13 | 2 × Class D |

`[F]` — Source: Eurosafe / Safelock Systems lock-to-safe mapping. This is why "which lock grade do I need" is usually answered by "which body grade do you need first."

---

## Selection Decision Framework

Work the chain **safe type → threat model → body grade → lock grade**, never "pick a lock, then find a safe":

1. **Define the threat.** Casual smash-and-grab (5–10 min, hand tools) vs. professional tool attack (drills, cutting, torch) vs. insider/manipulation risk vs. armed-robbery time pressure.
2. **Pick the body grade** ([full breakdown](safe-burglary-ratings-decoded.md)): residential → UL 1037 RSC or EN 14450 S1/S2; commercial → UL 687 TL-15/TL-30 or EN 1143-1 Grade 0–5; high-security → TRTL/TXTL or Grade 6+.
3. **Pick the lock grade to match**: Group 2 / Type 1 / Class A for residential; Group 1/1R or Class B/C for commercial; Class D for the highest tiers.
4. **Then choose the *family*** on operational grounds: mechanical dial for no-power reliability, key for a simple secondary lock, time-delay for armed-robbery deterrence, electronic for speed + audit, biometric only if sensor quality is proven.

| Your situation | Lock family | Grade to require |
|---|---|---|
| Long-term storage, rarely opened, no power dependence | Mechanical dial | Group 2 or Class A (residential); Group 1/1R or Class B/C (commercial) |
| Daily access, multiple users, want an audit trail | Electronic keypad | UL Type 1 or Class B/C |
| Banking / controlled-substance (US) | Mechanical dial | **Group 1R + TL-30 body** (DEA) |
| Retail / cash-holding with robbery risk | Electronic time-delay | Type 1 or Class B/C with time-delay |
| Dual-lock high-grade safe | Mechanical dial + key (secondary) | Match primary to body grade |

---

## Professional Repair & Maintenance

- **Battery discipline (electronic):** replace batteries on a schedule, *before* the low-battery warning, and confirm the model uses non-volatile memory so a dead battery never erases the code `[F]`.
- **Dial servicing (mechanical):** periodic professional lubrication and re-verification of the combination; a Group 1 lock's adjustable wheel-pack torque is a service point, not user-serviced.
- **Change the factory default combination immediately** — a safe left on the manufacturer default is a statistical gift.
- **Key control:** restricted keyways and a logged key register are the entire security story for key locks.
- **Failure recovery:** most electronic-lock failures are the external keypad, replaceable without drilling the safe (Liberty Safe) `[F]`; mechanical locks rarely fail but require a licensed professional when they do.

---

## The Author's Take

**My position: stop choosing a safe lock by "mechanical vs electronic" first — choose by grade first, then by family, and never let anyone sell you a "biometric" or "million combinations" label as a substitute for a tested grade.** Three points:

1. **Grade is the only honest currency.** A "biometric" lock with no UL Type 1 or EN 1300 certification is an uncertified electronic lock with a fingerprint sensor attached — the sensor does not raise the security ceiling. A Group 2 dial and a Type 1 electronic lock are both "residential-grade"; the real decision below the grade is *failure mode*, not *security*.
2. **The Group 2M / Group 1R conflation is a genuine, common error** — "2M" is two hours of manipulation resistance, and only "1R" carries the radiological (X-ray) rating that the DEA actually requires. If you are buying for controlled-substance compliance, verify "Group 1R," not "2M," and know that electronic locks do not satisfy that specific US regulatory requirement.
3. **In the European system the lock grade is *dictated* by the body grade** (EN 1143-1 Grade 0–2 require Class A, Grade 6+ require Class C, and so on). That coupling is the cleanest way to avoid the classic mistake of pairing a great lock with a weak body — North American buyers have to make that check manually.

**Conclusion:** read the body grade first, then require the matching lock grade, then pick the family that fits your access pattern and failure tolerance. Grade is the decision; family is the preference.

(Disclosure: this is the author's professional interpretation of the published UL 768 / UL 2058 / EN 1300 standards and manufacturer/trade documentation cited below — not first-party test data, and not regulatory or insurance advice.)

---

## FAQ

**What are the families of safe locks?**
Mechanical dial (combination), mechanical key, time lock/time-delay, electronic keypad, and biometric. Biometric is an electronic lock with a biometric credential, not a separate security tier.

**UL 768 Group 2M — what does the "M" mean?**
Manipulation. Group 2M is rated for 2 working hours of manipulation resistance. Radiological (X-ray) resistance is Group 1R, not 2M.

**Which lock grade does the US DEA require for controlled substances?**
UL Group 1R mechanical lock paired with a TL-30 safe. Electronic locks do not meet this specific DEA requirement.

**What is EN 1300 Class A/B/C/D?**
The European high-security lock classification: A (lowest) through D (highest), covering key, mechanical combination, and electronic locks, with reliability tests (10,000 cycles).

**Does a biometric lock's fingerprint sensor make it more secure?**
No — security comes from the lock's tested grade (UL Type 1 / EN 1300), not the sensor. Verify the grade, not the "biometric" label.

**Is a lock's grade the same as the safe's grade?**
No. The lock grade measures non-destructive-opening resistance (UL 768/2058, EN 1300); the body grade measures forced-entry resistance (UL 1037/687, EN 14450/1143-1).

---

## Sources

- **UL 768** — [Lockwiki: UL 768](https://www.lockwiki.com/index.php/UL_768) (Group 2/1/1R definitions, dialing tolerances, 1M combinations, 20-hour manipulation, Group 1R radiological ≤10 curies cobalt-60 at 30", punching immobilization). Accessed 2026-09-12.
- **UL 2058** — Safe & Vault Store, "Mechanical vs Electronic vs Biometric Safe Locks" (single Type 1 grade; no key override; DEA Group 1R + TL-30 requirement; SecuRam/LaGard/S&G). Accessed 2026-09-12.
- **EN 1300** — [Safelock Systems, "Certification"](https://safelocksystems.co.uk/knowledgebase/general-info/certification) (Classes A–D, 10,000 cycles / 100 code changes, La Gard 1947 dial-dependency, ECBS lock list). Accessed 2026-09-12.
- **EN 1300 lock-to-safe mapping** — [Eurosafe, "Lock Standards EN 1300"](https://www.eurosafe-online.com/lock-standards-en1300) (grade → required lock class table). Accessed 2026-09-12.
- **ECBS** — European Certification Body GmbH, Lock Guide ECB•S R01 (March 2017), EN 1300 certified lock list.
- **Time-delay / duress** — [Wikipedia: Time-delay combination locks](https://en.wikipedia.org/wiki/Time-delay_combination_locks); Sargent & Greenleaf time-lock product documentation (two-movement mechanical time lock). Accessed 2026-09-12.
- **Key lock UL Type 1/Type 2** — Kcolefas, "Safe Locks: The Definitive Guide" (Type 1 ≥20h manipulation + 60min forcing; Type 2 ≥30min; audit trails). Accessed 2026-09-12.
- **Electronic failure / keypad replacement** — Liberty Safe, "Electronic vs Mechanical" (keypad is the common failure point, replaceable without drilling). Accessed 2026-09-12.

> Data labeling: `[F]` = published standard/manufacturer fact; `[D]` = derived or industry-experience figure. No figures here are first-party test data. Standards (UL 768/2058, EN 1300) are subject to revision — verify the current edition before any regulated or insured purchase.

## 关联

- → [Mechanical vs Electronic Safe Locks](mechanical-vs-electronic-safe-locks.md)（可靠性 vs 便利，失效模式）
- → [Safe Burglary Ratings Decoded](safe-burglary-ratings-decoded.md)（柜体 UL 687 / EN 1143-1 等级）
- → [Lock Security Standards Explained](../standards/lock-security-standards-explained.md)（标准总览）
- → [Lock Technology Hub](../technology/index.md)（锁具机制）
- → Entity：`https://locktool.com/entity/safe-lock#entity` / `https://locktool.com/entity/ul-768#entity` / `https://locktool.com/entity/en-1300#entity`
