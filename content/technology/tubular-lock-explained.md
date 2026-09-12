---
title: "Tubular Lock Explained: The Radial Pin Tumbler Behind Vending Machines and Bike Locks"
description: "Tubular lock explained: how the radial pin tumbler mechanism works, pin counts and combinations, why dedicated tools make it overrated, and where tubular locks are still used."
---
# Tubular Lock Explained: The Radial Pin Tumbler Behind Vending Machines and Bike Locks

> Project: Locktool · Content
> Type: Technical Explanation Cluster (Template B)
> Hub: Lock Technology Hub (/technology/)
> Primary entities: `https://locktool.com/entity/tubular-lock#entity`, `https://locktool.com/entity/lock#entity`
> Status: PUBLISHED
> Research date: 2026-09-12 · Source tier: Tier 1 (Wikipedia / Chicago Lock Co. catalogs) + Tier 2 (LockPickWorld, locksmith industry)

---

## Quick Answer

A **tubular lock** (also called an Ace lock or radial lock) is a **radial variant of the pin tumbler** — it still aligns spring pins at a shear line, but the pins are arranged in a **ring around a central axis** instead of linearly, driven by a **cylindrical key** (cut around its edge).

It's widely assumed to be "more secure than a standard lock" because ordinary tools can't reach it. The truth: a **dedicated tubular tool can open it in seconds to a couple of minutes**. Its security rating is commonly **medium (3/5) — it needs the right tool, but once you have that tool it's easy**. Typical applications: vending machines, ATMs, arcade games, elevators, bicycle locks, computer locks, and coin-operated equipment.

---

## Definition

**Tubular lock** — a pin tumbler lock whose spring pin pairs are arranged **radially in a ring** around a central axis and driven by a **cylindrical key** with cuts around its edge; also called an Ace lock or radial lock.

---

## Mechanism: Pins Arranged in a Ring

A tubular lock's underlying principle is identical to a standard pin tumbler — **key pin + driver pin + spring separating at the shear line**. The only difference is geometry:

| Dimension | Standard pin tumbler | Tubular lock |
|---|---|---|
| Pin arrangement | Linear (single row) | Radial (ring around central axis) |
| Pin orientation | Vertical | Horizontal (facing forward) |
| Pin count | Usually 5–6 | Usually 7, 8, or 10 |
| Key | Flat blade, edge teeth | Cylindrical, ring of edge cuts |

When the correct key inserts, the edge cuts push each radial pin to the correct depth, all pins align with the shear line, and the plug rotates. Each notch on the key's inner edge depresses a single pin to a specific height.

### Combination Count

A 7-pin tubular lock with 4 depth steps per pin yields 4⁷ = **16,384 theoretical combinations** `[D]` — fewer in practice, because manufacturers use only a subset and many budget units are keyed alike. This is a middle band: higher than wafer, far lower than a high-end disc detainer.

---

## Why It's Mistaken for "Secure" — and Why Dedicated Tools Defeat It Quickly

**Where the public misjudgment comes from**: tubular locks appear on coin boxes and vending machines, so they look "industrial-grade," and ordinary hooks/rakes genuinely don't fit the round keyway.

**The reality**: a dedicated **tubular tool** exists — a cylindrical tool with a ring of needles that, when inserted with torque and a rocking motion, works each pin into shear-line alignment, usually opening the lock in seconds to a minute or two.

Key points:
1. **Ordinary tools fail, but dedicated tools are efficient** — this is the biggest difference from pin tumbler. A standard pin tumbler is picked slowly with general tools; a tubular lock needs (and only needs) a size-matched tubular tool.
2. **Lower depth sensitivity** — a design trait often cited within the tubular community, where key-depth dependence is lower, which is one reason it suits frequently-cycled coin devices.
3. **Legacy 7-pin vs. upgraded 8/10-pin** — most field units are **7-pin**, the legacy standard for vending and bike applications; higher-security versions move to 8 or 10 pins and sometimes add **false notches** in the pin stacks (as on the Chicago ACE II) to resist single-pin work `[F]`.

So its security rating is "**requires the correct tool**," not "high security." The locksmith industry commonly lists it at **3/5 (moderate, needs dedicated tools)**.

---

## Failure Modes

| Failure mode | Cause | Field symptom |
|---|---|---|
| Spring fatigue | Long-term cycling in high-use coin devices | Pins no longer return crisply; key works intermittently |
| Pin tip wear | Frequent operation + grit | Key jiggles before turning |
| Key deformation | Thin cylindrical key bent in pocket or use | Key won't seat or turns with resistance |
| Central post wear | Repeated key insertion | Loose key seating; imprecise alignment |

---

## The Author's Take

**Position:** The tubular lock is an "overrated" mechanism — its security rests on "the tool isn't common," not "the mechanism resists manipulation."

**Reasoning:**
1. Once an attacker has a size-matched tubular tool, its protection nearly vanishes. This is fundamentally different from a disc detainer, which resists via the mechanism itself (false gates + DBS): disc detainer is "mechanism-hard," tubular is "tool-gated."
2. It's not that tubular is useless — it's that its value is correctly scoped to *low-value + frequent cycling + deter casual opening*, not to *high-value asset protection*.
3. The uprated 8/10-pin ACE II variants with false notches are better, but still don't change the "tool-gated" category — they raise the bar for that one tool, not the mechanism class.

**Disclosure:** This is my professional judgment based on mechanism analysis and locksmith industry consensus — an opinion, not a verified empirical test result.

So my advice: **the tubular lock suits "low-value + frequent cycling + deter casual opening" contexts (coin devices, elevators, ordinary bicycles), but not as the first line of defense for high-value assets.** If you're protecting high-value equipment, don't rely on a tubular.

---

## FAQ

**What is a tubular lock?**
A radial pin tumbler with pins arranged in a ring, driven by a cylindrical key. Also called an Ace lock or radial lock.

**Is a tubular lock secure?**
Medium (3/5). Ordinary tools struggle, but a dedicated tubular tool can open it quickly, so it doesn't suit high-security contexts.

**Where is it used?**
Vending machines, ATMs, arcade games, elevators, bicycle locks, computer locks, coin-operated devices.

**How many pins does it have?**
Usually 7, 8, or 10, evenly spaced around the ring. The 7-pin version is the legacy standard.

**How many combinations does a 7-pin tubular lock have?**
4⁷ = 16,384 theoretical (assuming 4 depth steps), fewer in practice because manufacturers use a subset and many budget units are keyed alike.

---

## Sources

- [Wikipedia — Tubular pin tumbler lock](https://en.wikipedia.org/wiki/Tubular_pin_tumbler_lock) (accessed 2026-09-12) — radial mechanism, cylindrical key, Ace/radial terminology.
- [LockPickWorld — Tubular Locks Explained](https://www.lockpickworld.com/pages/tubular-locks-explained) (accessed 2026-09-12) — 7/8 pin stacks in a circle, legacy 7-pin standard, false notches on higher-security variants.
- [Chicago Lock Company No. 173 catalog](https://s3.amazonaws.com/s3-absupply-net/pdf/vintage-catalogs/chicago-company/chicago-lock-company-no-173-ocr-1973.pdf) (primary catalog, accessed 2026-09-12) — ACE 7-pin/10-pin tumbler locks, keyed-alike options.
- SouthOrd — Beginner's Guide to Tubular Lock Picking (mechanism, tubular tool principle).
- ITS Tactical — Tubular Lock Picking (7/8/10 pin configurations, tools).

> Data labeling: key figures above are marked `[F]` (source fact) or `[D]` (industry-derived/experience). Anything in the Author's Take is our own inference, explicitly labeled as professional judgment rather than source fact.

> Research date: 2026-09-12 · Accessed: 2026-09-12. Sources are third-party authorities and manufacturer public material, not our own testing. Regulatory information may become outdated; always verify current local requirements before acting.

## Related

- → Pillar: [Pin Tumbler vs Wafer vs Disc Detainer](pin-tumbler-vs-wafer-vs-disc-detainer.md)
- → [Pin Tumbler Lock: How the Mechanism Works](pin-tumbler-lock-explained.md) (the linear parent mechanism)
- → [Lock Type Comparison Matrix](../lock-type-comparison-matrix.md)
- → Entities: `https://locktool.com/entity/tubular-lock#entity` / `https://locktool.com/entity/lock#entity`
