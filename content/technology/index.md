# Lock Technology

**Quick Answer:** A lock mechanism is the mechanical system that blocks a rotating plug or a sliding bolt until the correct key aligns its internal parts. The seven core mechanical families — pin tumbler, wafer, disc detainer, dimple, tubular, lever, and warded — differ in *what* blocks the plug and *how* the key releases it, which is why they occupy different security, cost, and application bands.

## What This Hub Covers

Every article here explains **how a mechanism works** — the engineering of shear lines, gates, sidebars, false gates, and levers — so locksmiths, security technicians, specifiers, and buyers can make informed decisions. This is education, not attack instruction: we explain the *defense* mechanism (what resists picking, bumping, drilling, and snapping), never step-by-step bypass or defeat techniques.

Each article follows a fixed structure so it is machine-retrievable and human-useful:

1. **Quick Answer** — one to two sentences an AI or reader can extract verbatim.
2. **Definition block** — a single bolded sentence defining the mechanism.
3. **Mechanism** — how the blocking element, key, and unlock condition work.
4. **Engineering parameter table** — combinations, tolerance, and failure modes, normalized.
5. **The Author's Take** — a first-person engineering judgment (Position / Reasoning / Disclosure).
6. **Sources** — authoritative URLs with access dates, labeled `[F]` (fact) or `[D]` (derived).

## Core Articles

| Article | Type | Read If You Want To… |
|---|---|---|
| [Pin Tumbler vs Wafer vs Disc Detainer](pin-tumbler-vs-wafer-vs-disc-detainer.md) | Comparison Pillar | Understand the three core mechanisms side by side, with a decision framework |
| [Pin Tumbler Lock Explained](pin-tumbler-lock-explained.md) | Technical | Grasp combination math, MACS, tolerance, and security pins |
| [Wafer vs Pin Tumbler](wafer-vs-pin-tumbler.md) | Comparison | See why wafer is the lowest-security common lock, and when that's fine |
| [Disc Detainer Locks Explained](disc-detainer-locks-explained.md) | Technical | Understand false gates, DBS, and why Abloy's ~1.9-billion-combination Protec2 is hard to manipulate |
| [Dimple Lock Explained](dimple-lock-explained.md) | Technical | Learn the flat-face pin tumbler variant, Mul-T-Lock telescopic pins, and the Euro-cylinder snap weakness |
| [Tubular Lock Explained](tubular-lock-explained.md) | Technical | See why the radial pin tumbler is "tool-gated" security, not mechanism-hard security |
| [Lever Tumbler Lock Explained](lever-tumbler-lock-explained.md) | Technical | Understand the 1778 Barron mechanism, the 1818 Chubb detector, and BS3621 |

## Key Mechanism Facts at a Glance

| Mechanism | Blocking element | Unlock condition | Typical combinations | Relative manipulation resistance |
|---|---|---|---|---|
| Wafer | Flat spring-loaded wafer | Wafers flush with plug edge | Low (4-wafer × 4-depth = 256 `[D]`) | Lowest (rake/jiggler-prone) |
| Pin tumbler | Key pin + driver pin pair | Pin joints align at shear line | 5-pin 10-depth = 100,000 theoretical; 30k–50k usable `[D]` | Low–medium (upgradeable via security pins) |
| Tubular | Radial pin pair ring | Radial pins align at shear line | 7-pin ≈ 16,384 theoretical `[D]` | Medium (dedicated tools defeat it) |
| Dimple | Side-pinned pin pairs (± side pins) | Pins align on flat key face | Medium–high (multi-row + telescopic pins) | Medium–high |
| Lever | Lever + gate + bolt stump | Gates align into one channel | Medium (5-lever is BS3621 floor) | High (with false notches + curtain + relocker) |
| Disc detainer | Rotating discs + sidebar | True gates align into a channel | Highest (Protec2 ≈ **1.9–1.97 billion** `[F]`) | Highest (DBS + false gates) |

> The Protec2 figure is **billion, not million**: 11 discs with 7 cut angles each give 7¹¹ ≈ 1.98 billion theoretical combinations (Abloy's public claim is "1.9 billion"; Locksmith Ledger reports "1.97 billion"). An earlier draft of this hub misstated it as "190 million" — a 10× understatement, now corrected. `[F]`/`[D]` labels separate source facts from derived values; see each article for full citations.

## How the Mechanisms Relate

```
Lock ── has-mechanism ──▶ Pin Tumbler ── variant-of ──▶ Dimple (flat-face)
    │                                        └─ variant-of ──▶ Tubular (radial)
    ├── has-mechanism ──▶ Wafer
    ├── has-mechanism ──▶ Disc Detainer
    └── has-mechanism ──▶ Lever
```

- Pin tumbler is the "root family": dimple and tubular are geometric re-arrangements of the same pin-and-shear-line principle.
- Wafer, disc detainer, and lever are distinct blocking principles — no pins, different failure physics.
- This family tree is why "more pins" and "more discs" are not directly comparable across branches.

## The Author's Take

**Position:** When you're choosing a lock, the first question is *never* "which mechanism ranks highest" — it's "what am I actually defending against, and against whom?"

**Reasoning:**
1. The six mechanisms here don't sit on a single good-to-bad line; each occupies a cost, durability, and threat-model band. A wafer lock on a drawer is not a "weak lock" — it's the *correct* lock for that job.
2. The single most dangerous buyer error I see is picking by one number (combinations or pin count). Manipulation resistance is a product of tolerance, security features, and build quality, not a headline figure.
3. The Protec2's ~1.9-billion-combination figure is real but nearly beside the point: no attacker opens one by trying keys — its defense is the mechanism, not the number.

**Disclosure:** This is my professional judgment based on mechanism engineering and public manufacturer/standards data — an opinion, not a verified empirical test result.

## Related Hubs

- [Tools & Equipment](../tools/index.md) — which locksmith tools interact with each mechanism (taxonomy, picks, decoders, key machines).
- [Standards & Compliance](../standards/index.md) — how ANSI/BHMA grades, EN 1303, and UL 437 rate these mechanisms.
- [Lock Type Comparison Matrix](../lock-type-comparison-matrix.md) — the single normalized cross-hub reference table.
