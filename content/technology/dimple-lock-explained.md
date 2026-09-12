---
title: "Dimple Lock Explained: How Side-Pinned Pin Tumblers Work and Where They Sit on the Security Ladder"
description: "Dimple lock explained: how the side-pinned pin tumbler mechanism works, telescopic pins, the DHF star system, EN 1303 key-related grades, and the snap-attack weakness."
---
# Dimple Lock Explained: How Side-Pinned Pin Tumblers Work and Where They Sit on the Security Ladder

> Project: Locktool · Content
> Type: Technical Explanation Cluster (Template B)
> Hub: Lock Technology Hub (/technology/)
> Primary entities: `https://locktool.com/entity/dimple-lock#entity`, `https://locktool.com/entity/lock#entity`
> Status: PUBLISHED
> Research date: 2026-09-12 · Source tier: Tier 1 (DHF/GGF star system, EN 1303) + Tier 2 (Mul-T-Lock manufacturer, locksmith industry)

---

## Quick Answer

A **dimple lock** is a **variant of the pin tumbler lock** — it still uses spring pins and a shear line, but the pins are driven from the **flat face of the key rather than its edge**.

The key inserts and rotates 90°, using the **flat of the key blade** (not the edge teeth) as the driving surface, with a pattern of bumps/dimples pressing the pins. Because the cuts sit on a flat plane, they can be packed more densely and support **side pins**, telescopic "pin-in-pin" stacks, and extra dimensions, so dimple locks are generally **more pick-resistant than ordinary edge-cut pin tumblers**, sitting in the "medium to high" security band. The most common application is the **Euro cylinder** and high-security padlocks.

---

## Definition

**Dimple lock** — a pin tumbler lock whose key drives the pins from the **flat face** of the blade (via bumps/dimples) rather than from the edge teeth, allowing higher pin density and additional pin dimensions such as side pins and telescopic pins.

---

## Mechanism: From "Edge Teeth" to "Flat-Face Cuts"

An ordinary pin tumbler drives pins from the key's **edge teeth**, with pins aligned along the key edge.

A dimple lock's key is also flat, but its **cuts are on the flat face** — little bumps or dimples that, after a 90° rotation, press against **side-mounted pins**.

Because a flat face can carry more cuts in freer arrangements, dimple locks typically accommodate:
- More pins (high-end Euro cylinders can reach 11 pins)
- **Side pins** / **sidebars**, adding a second dimension of defense
- More complex keyways, restricting tool entry angles

Dimple locks are therefore often harder to pick than an edge-cut pin tumbler with the same pin count, and require **dedicated dimple picks** — ordinary hooks/rakes don't fit.

### The Telescopic "Pin-in-Pin" Variant (Mul-T-Lock)

The most famous dimple-family innovation is Mul-T-Lock's **telescopic pin** design (founded 1973 `[F]`): each pin position holds an **outer pin with a smaller inner pin nested inside it**. Both the inner and outer pin must reach their own shear lines simultaneously for the plug to turn — the Interactive+ platform uses **5 inner + 5 outer pin pairs** `[F]`. This "pin-within-a-pin" geometry sharply raises manipulation difficulty without adding pin positions, and larger versions add **passive key-control side pins** that interact with a sidebar for a third locking dimension `[F]`.

---

## Engineering Parameters

| Parameter | Edge-cut pin tumbler (typical) | Dimple lock (typical / high-end) |
|---|---|---|
| Pin drive surface | Key edge teeth | Key flat face (bumps/dimples) |
| Pin count | 5–6 | 5–11 (multi-row) |
| Extra dimensions | Rarely | Side pins, telescopic inner/outer pins, sidebars |
| Key insertion | Linear | Insert + rotate 90° to engage |
| Tooling | Standard hooks/rakes | Dedicated dimple picks required |
| Manipulation resistance | Low–medium | Medium–high |

---

## Security Grades & the Star System (Euro Cylinder Context)

Dimple locks appear heavily in Euro cylinders, which carry a **1–3 star rating** maintained by the **DHF (Door & Hardware Federation) and the Glass & Glazing Federation**:

| Star rating | Typical configuration | Attack resistance |
|---|---|---|
| 1-star | 6 pins | Basic pick resistance, but vulnerable to bump / snap (cylinder snapping) attacks |
| 3-star | 11 pins + anti-snap / anti-bump / anti-drill | Resists picking, drilling, extraction, bumping, and snapping; Secure by Design certified |

**Key note**: the Euro cylinder's **greatest weakness is not the pin mechanism but "lock snapping"** — violently breaking the cylinder to expose the internal mechanism. This is the most common attack on 1-star low-security Euro cylinders, and 3-star cylinders solve it with anti-snap designs (a sacrificial section that breaks away while the locking mechanism stays secure).

### Star Rating × Attack Vector Matrix

The star rating maps directly to specific attack vectors, not to a vague "security" label. This table makes that mapping explicit:

| Attack vector | What it targets | 1-star (6-pin) | 3-star (11-pin, anti-*) |
|---|---|---|---|
| **Picking** | Manipulates pins to align the shear line | Partial (no security pins) | Resists (multi-pin + anti-pick design) |
| **Bumping** | Strikes pins so driver pins momentarily clear the shear line | Vulnerable | Resists (anti-bump) |
| **Drilling** | Bores through the cylinder/housing | Vulnerable | Resists (anti-drill inserts + hardened pins) |
| **Snapping** | Breaks the cylinder at its fixing point to expose the mechanism | **Vulnerable (most common)** | Resists (anti-snap sacrificial section) |
| **Plug extraction** | Pulls the plug out to bypass the pins | Vulnerable | Resists (anti-extraction) |

### EN 1303: Key-Related Security Grades

Beyond the DHF star system, the European standard **EN 1303** classifies cylinders with a multi-digit code. Two digits matter most for dimple/Euro cylinders:

- **Key-related security** — grades 1–6, where **grade 6** is highest. Grade 6 requires a minimum of **100,000 effective differs** and a minimum of **6 movable blocking parts** `[F]`.
- **Attack resistance** — grades 0/A/B/C/D, where **D** is highest (resistance to drilling, chisel, twisting, and plug/cylinder extraction) `[F]`.

> The single most important upgrade decision in a Euro cylinder is **snap resistance**, not pin count. A 6-pin 1-star cylinder and an 11-pin 3-star cylinder differ most dramatically on snapping — the attack most often used against exposed UK/EU lock cylinders. Pin count is secondary to the anti-snap design.

---

## Failure Modes

| Failure mode | Cause | Field symptom |
|---|---|---|
| Telescopic pin jamming | Dirt/grit in the inner-pin nesting | Inner pin sticks; key feels "crunchy" |
| Key wear on flat face | Repeated insertion against side pins | Dimples wear shallow; lock fails to engage |
| Cylinder snapping (Euro body) | Exposed fixing point + weak body | Whole front section breaks off, exposing mechanism |
| Spring fatigue | Long-term cycling | Pins no longer return crisply |

---

## The Author's Take

**Position:** The dimple lock is "an advanced branch of the pin tumbler family" — its value is trading a flat-face cut for higher pin density and side-pin dimensionality, but it is not a fundamentally new security paradigm.

**Reasoning:**
1. If you want "more pick resistance than a standard door lock but still within the pin tumbler system," dimple is the right choice — the telescopic pin-in-pin design in particular raises difficulty without adding bulk.
2. But it still faces bump / snap threats that must be addressed through the star system's anti-snap / anti-bump designs — not by the fact that "it's a dimple" alone.
3. The telescopic mechanism also introduces a *new failure mode* (inner-pin jamming from grit) that a simple edge-cut cylinder doesn't have — a real maintenance consideration for outdoor installations.

**Disclosure:** This is my professional judgment based on mechanism analysis, the DHF rating system, and manufacturer public specifications — an opinion, not a verified empirical test result.

So when choosing a Euro cylinder, **the star rating (1-star vs 3-star) and the EN 1303 key-related grade matter more than "is it a dimple"** — the rating directly maps to specific anti-snap / anti-bump / anti-drill capability.

---

## FAQ

**How does a dimple lock differ from a standard pin tumbler?**
Same mechanism (spring pins + shear line), but pins are driven from the key's flat face, allowing more pins and side pins, higher pick resistance, and requiring dedicated tools.

**Is a dimple lock more secure?**
Within the pin tumbler system, yes. But it still faces bump/snap threats; security depends on the star rating and anti-attack design, not the "dimple" label itself.

**What is the telescopic pin (Mul-T-Lock) design?**
Each pin position holds an outer pin with a smaller inner pin nested inside; both must reach their shear lines simultaneously. The Interactive+ uses 5 inner + 5 outer pairs.

**What are the 1-star and 3-star Euro cylinder ratings?**
A rating system from the DHF + Glass & Glazing Federation. 1-star offers basic pick resistance; 3-star resists pick / drill / extraction / bump / snap and is Secure by Design certified.

**What does EN 1303 key-related grade 6 mean?**
The highest key-related security grade, requiring a minimum of 100,000 effective differs and 6 movable blocking parts.

---

## Sources

- [Mul-T-Lock — Interactive Platform](https://www.mul-t-lock-online.com/store/index.php?dispatch=pages.view&page_id=9) (official, accessed 2026-09-12) — telescopic pin-in-pin mechanism, inner/outer pins.
- [Lockwiki — Mul-T-Lock Interactive+](https://www.lockwiki.com/index.php/Mul-T-Lock_Interactive%2B) (accessed 2026-09-12) — 5 inner + 5 outer pin pairs.
- [Coastal Group / DHF-GGF star system](https://www.eros-secure.co.uk/wp-content/uploads/2024/01/BS-EN-1303.pdf) — BS EN 1303 key-related grades and attack-resistance grades (0/A/B/C/D).
- [Lockwiki — EN 1303](https://www.lockwiki.com/index.php/EN_1303) (accessed 2026-09-12) — key-related security grades 1–6, durability grades 4/5/6.
- Master Key Systems — Euro Cylinder Locks Explained (dimple mechanism, 11-pin 3-star vs 6-pin 1-star).
- LockPickWorld — Pin Tumbler Locks Explained (dimple comparison).
- Wikipedia — Pin tumbler lock (dimple side pin reference).

> Data labeling: key figures above are marked `[F]` (source fact) or `[D]` (industry-derived/experience). Anything in the Author's Take is our own inference, explicitly labeled as professional judgment rather than source fact.

> Research date: 2026-09-12 · Accessed: 2026-09-12. Sources are third-party authorities and manufacturer public material, not our own testing. Regulatory information may become outdated; always verify current local requirements before acting.

## Related

- → Pillar: [Pin Tumbler vs Wafer vs Disc Detainer](pin-tumbler-vs-wafer-vs-disc-detainer.md)
- → [Pin Tumbler Lock: How the Mechanism Works](pin-tumbler-lock-explained.md) (deep dive)
- → [EN 1303 Decoded](../standards/en-1303-decoded.md)
- → [Lock Type Comparison Matrix](../lock-type-comparison-matrix.md)
- → Entities: `https://locktool.com/entity/dimple-lock#entity` / `https://locktool.com/entity/lock#entity`
