---
title: "Electric Strike vs Maglock: Holding Force, Fail Behavior, Cycles, and Door Fit Compared"
description: "Electric strike vs maglock compared on the numbers that matter: holding force, static/dynamic strength, fail-safe vs fail-secure, cycle life, door types, and ANSI/BHMA grades — with a door-by-door decision framework."
---
# Electric Strike vs Maglock: Holding Force, Fail Behavior, Cycles, and Door Fit

> 项目：Locktool · Content
> 类型：Comparison Cluster（模板 A/C）
> 所属 Hub：Access Control Hub（/access-control/）
> 主实体：`https://locktool.com/entity/electric-strike#entity`、`https://locktool.com/entity/maglock#entity`
> 状态：UPGRADED v0.2
> 研究日期：2026-09-12

---

## Quick Answer

Electric strikes and maglocks both unlock a door electrically, but they are **different mechanisms with different failure modes and different doors**. A strike is a frame-mounted keeper that releases the existing mechanical latch and can be **fail-safe or fail-secure**; a maglock is an electromagnet-and-armature that is **inherently fail-safe**. Choose by **door material first, then fail-mode and code, then strength numbers.**

> **Definition — Electric Strike:** a frame-mounted, electrically operated keeper that releases a mechanical lock's latch/bolt when energized, replacing the standard strike plate; listed to **ANSI/BHMA A156.31**.
> **Definition — Maglock (Electromagnetic Lock):** a frame-mounted electromagnet plus a door-mounted steel armature that holds the door closed by magnetic force; listed to **ANSI/BHMA A156.23**. Inherently fail-safe — it releases the instant power is removed.

## The Engineering Comparison

| Dimension | Electric Strike | Maglock |
|---|---|---|
| Mechanism | Frame keeper releases existing latch/bolt | Electromagnet holds a steel armature plate |
| Holding mechanism | The **mechanical latch** still holds; strike controls release | **Magnetic force** alone holds the door |
| Fail behavior | **Selectable** fail-safe or fail-secure | **Inherently fail-safe** (always) |
| Power's role | Applied to **release** (fail-secure) or **hold** (fail-safe) | Applied continuously to **hold** |
| Standard | ANSI/BHMA **A156.31** | ANSI/BHMA **A156.23** |
| Typical doors | Metal/wood with an existing latch/bolt | Glass, aluminum-frame, frameless, high-traffic |
| Mechanical egress | Keeps lever/panic hardware | **None** — requires REX device |
| Fire-rated opening | Fire-rated strikes are **fail-secure only** | Requires REX + fire-alarm release |
| Representative strength | Static 1,500–2,500+ lb; dynamic 70–350 ft-lb | Holding force 600–1,200 lb (shear locks 2,000–2,700 lb) |

## The Numbers, With Sources

**Electric strike strength (ANSI/BHMA A156.31).** Grade is set by cycle testing plus static and dynamic strength. A156.31-2024 requires a **Grade 1 strike to pass 500,000 cycles** [F]. Top commercial strikes exceed this by a wide margin — ASSA ABLOY's HES 1006 series is spec'd at **2,500 lb static strength (tested past 3,000 lb), 350 ft-lb dynamic strength (fail-secure), and 1,000,000+ cycles**, with UL 1034 and UL 294 listings [F]. A lighter-duty 5200-series Grade 1 strike specs **1,500 lb static / 70 ft-lb dynamic / 500,000 cycles** [F]. The spread matters: static strength is the door's resistance to being *shoved* open, dynamic strength its resistance to *impact*.

**Maglock holding force (ANSI/BHMA A156.23).** A156.23 requires **Grade 1 maglocks to withstand 1,000,000 cycles** while continuing to meet electrical and strength requirements [F]. Holding force is the headline spec: common security maglocks run **600–1,200 lb**; shear locks reach **2,000–2,700 lb** (SDC [F]). The critical SDC guidance already flagged in this cluster: **a maglock under 1,200 lb holding force is only suitable for traffic control, not as a security lock** — treat that number as a floor, not a goal.

## Two Decision Variables That Override Brand

### 1. Fail mode (the compliance variable)
- **Strike** is the flexible choice: field-selectable fail-safe **or** fail-secure. Most deployments are fail-secure (Axis [F]).
- **Maglock** is always fail-safe. If the door must *stay locked* on power loss (server room, perimeter), a maglock is the wrong tool — no configuration changes its physics.

### 2. Door material and egress (the physical variable)
- **Strike** requires a frame and an existing latch/bolt — glass or frameless aluminum doors are out.
- **Maglock** fits glass/frameless doors, but has **no mechanical egress**, so code (NFPA 101 access-controlled egress; IBC sensor release) requires a **REX device or motion sensor** plus **fire-alarm release**. Skip the REX and you have an inspection failure, not a minor omission.

## The Fire-Door Constraint (Often Missed)

A **fail-safe electric strike cannot be used on a fire-rated opening**: with power off it doesn't positively latch, so the door loses its fire/smoke barrier (HES fire-rating is **fail-secure only** — UL 10C 3-hour [F]). If you need an electric strike on a fire door, it must be the **fail-secure** variant listed for the door's rating. Maglocks on fire doors likewise need the full REX + fire-alarm release treatment.

## Door-by-Door Decision Framework

| Your scenario | Choose | Why |
|---|---|---|
| Office wood/metal door with existing latch/bolt | **Electric strike** (fail-secure default) | Keeps mechanical handle + latch; code-friendly egress |
| Glass / aluminum-frame / frameless / storefront | **Maglock** | No frame to cut a strike into |
| High-traffic lobby / automatic door | **Maglock** | Fail-safe matches egress; no moving keeper to wear |
| Server room / storage that must stay locked in an outage | **Electric strike, fail-secure** | Maglock would unlock on power loss |
| Stairwell re-entry door | **Fail-safe strike or lockset** | Unlocks on fire alarm for re-entry |
| Fire-rated door needing electric control | **Fail-secure strike (fire-rated)** or fire-rated electrified lockset | Fire-rated strikes are fail-secure only |
| Perimeter/vehicle gate needing long read range | Neither — **UHF + gate hardware** | These are pedestrian-door locks |

## The Author's Take

**Position:** In my view, "electric strike vs maglock" is usually the wrong question — the door material and the egress code have already made the decision for you, and the only genuinely open choice is whether a strike should be fail-safe or fail-secure.

**Reasoning:** First, a frameless glass door physically cannot take a strike, and a wood door with a latch gets no benefit from a maglock's REX overhead — so in most openings the hardware is effectively pre-selected by the door. Second, the real risk lives in the fail-mode call, which is a fire-and-life-safety decision, not a preference: a fail-secure strike on an egress door is a liability, and a fail-safe strike on a fire door is a code violation. Third, on the strength numbers, buyers anchor on "1,200 lb" as a maglock's selling point when that's actually the *minimum* for a security lock — below it you've bought traffic control.

**Disclosure:** This is my professional opinion based on the ANSI/BHMA A156.31/A156.23 standards, manufacturer specifications (ASSA ABLOY/HES, SDC), and NFPA 101/IBC egress requirements cited below — not first-party testing.

## FAQ

**Is a maglock fail-safe or fail-secure?**
Inherently fail-safe — it releases the instant power drops. This is physics, not a setting.

**Can an electric strike go on a glass door?**
No. It needs a frame and an existing latch/bolt. Glass/frameless doors use maglocks.

**Does a maglock door always need a REX device?**
Yes, for egress doors. A maglock has no mechanical egress, so code requires a sensor or "PUSH TO EXIT" device plus fire-alarm release.

**What holding force should a security maglock have?**
1,200 lb or higher as a practical floor; below that it's traffic control, not security. Shear locks reach 2,000–2,700 lb.

**Can a fire-rated door use a fail-safe electric strike?**
No. Fire-rated strikes are fail-secure only — a fail-safe strike doesn't positively latch when unpowered.

## Sources

- BHMA — "A156.31-2024 Electric Strikes and Frame Mounted Actuators": http://buildershardware.com/ANSI-BHMA-Standards/Hardware-Highlights/A15631-2024-Electric-Strikes-and-Frame-Mounted-Actuators — Grade 1 = 500,000 cycles
- ASSA ABLOY / HES — "1006 Electric Strike" catalog: https://www.assaabloy.com/apac-blueprint/en/images/product-assets/sea-markets/electromechanical/electric-strike/1006-series/assets/documents/1006-series-electric-strike-catalog.pdf — 2,500 lb static / 350 ft-lb dynamic / 1M cycles; UL 1034, UL 294, UL 10C fail-secure only
- HES 5200 Series (Sweets Construction): http://sweets.construction.com/swts_content_files/56864/P288351.htm — 1,500 lb static / 70 ft-lb dynamic / 500,000 cycles, field-selectable fail mode
- BHMA — "ANSI/BHMA A156.23 Electromagnetic Locks" (Hardware Highlights): https://buildershardware.com/Portals/0/Files/2019%20Hardware%20Highlights/156.23%20HH%202019.pdf — Grade 1 = 1,000,000 cycles
- SDC Security — "Locking Devices: Electromagnetic Locks" catalog: https://www.sdcsecurity.com/docs/MagneticLocks-Catalog.pdf — 1,200 lb holding force, A156.23 Grade 1; 2,000/2,700 lb shear locks
- Axis — "Fail-safe vs fail-secure": https://newsroom.axis.com/en-us/blog/fail-safe-vs-fail-secure — strikes mostly fail-secure; mechanical override requirement
- Allegion / I Dig Hardware — "Decoded: Fail Safe vs Fail Secure" (2023-10): https://idighardware.com/2023/10/decoded-fail-safe-vs-fail-secure-when-and-where — fail-safe/secure refer to the secure side
- National Training Center — "Access Control – Egress Requirements": https://nationaltrainingcenter.com/access-control-egress-requirements — REX, PUSH TO EXIT, fire-alarm release
- Consulting-Specifying Engineer — "Door locking requirements in NFPA 101": https://www.csemag.com/door-locking-requirements-in-nfpa-101 — sensor release and delayed-egress rules

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上均为第三方权威标准组织/制造商/监管公开资料，非我方实测；关键数据按来源等级标注 `[F]`（事实）。静态/动态强度与吸力数值随型号与测试条件而异，以厂商最新规格与型号级测试报告为准。法规类信息随监管变化可能过期，执业前务必核实当地现行规定与 AHJ 执法口径。

## 关联

- → [Electronic Access Control Explained](electronic-access-control-explained.md)（全栈与 fail-safe/fail-secure 总览）
- → [Access Control Credentials Explained](access-control-credentials-explained.md)（凭证层，验证通过后触发本页的锁具）
- → [Fire-Rated Door Hardware Explained](../standards/fire-rated-door-hardware-explained.md)（防火门逃生硬件与 fail-safe 消防联动）
- → [ANSI/BHMA Grades Decoded](../standards/ansi-bhma-grades-decoded.md)（A156.x 分级如何读）
- → Entity：`https://locktool.com/entity/electric-strike#entity` / `https://locktool.com/entity/maglock#entity`
