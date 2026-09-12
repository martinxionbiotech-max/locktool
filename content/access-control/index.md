# Access Control

Electronic locks — electric strikes, maglocks, electrified locksets — and the fail-safe/fail-secure decision that governs them.

## Quick Answer

Electronic access control is a layered system — **credential → reader → controller → electrified lock → power/fire interface** — in which the lock is opened by a controller's power signal rather than a mechanical key. The single most consequential design decision in the whole stack is **fail-safe vs fail-secure**: what the door does when power is cut.

> **Definition — Electronic Access Control (EAC):** a system that gates entry using an electrically controlled locking device (electric strike, electromagnetic lock, or electrified lockset), released by a controller that validates a presented credential. The lock's "secure side" behavior on power loss is defined as *fail-safe* (unlocks) or *fail-secure* (stays locked).

## Core Articles

| Article | Type | Read If You Want To… |
|---|---|---|
| [Electronic Access Control Explained](electronic-access-control-explained.md) | Taxonomy Pillar | The credential → reader → controller → lock stack, plus the full standards map |
| [Access Control Credentials Explained](access-control-credentials-explained.md) | Cluster | 125kHz prox vs 13.56MHz MIFARE/DESFire vs Seos vs mobile — and why Wiegand is a protocol, not a card |
| [Electric Strike vs Maglock](electric-strike-vs-maglock.md) | Comparison | The engineering trade-off for the physical locking hardware |

## The Core Insight

The most overlooked design decision in electronic access control is **fail-safe vs fail-secure** — what the door does on the *access (secure) side* when power is removed:

| Mode | Behavior on power loss | Use it for |
|---|---|---|
| **Fail-safe** (unlock on power loss) | Door unlocks on the access side | Egress / fire routes, stairwell re-entry |
| **Fail-secure** (stay locked on power loss) | Door stays locked on the access side | Server rooms, storage, high-security areas |

Maglocks are **inherently fail-safe** (electromagnetism releases the instant power drops). Electric strikes and electrified locksets can be configured **either way**. Get this wrong and you create a life-safety violation — not a "spec preference."

## The Standards That Govern This Cluster

| Standard | Governs | Key concept |
|---|---|---|
| **ANSI/BHMA A156.31** | Electric strikes & frame-mounted actuators | Grade 1/2/3 via cycle + static/dynamic strength |
| **ANSI/BHMA A156.23** | Electromagnetic locks | Grade 1/2/3 via cycle + holding-force tests |
| **UL 294** | Access control system units | Destructive attack / line security / endurance / standby power, Levels I–IV |
| **UL 1034** | Burglary-resistant electric locking mechanisms | Strike listing for forced-entry resistance |
| **NFPA 101 / IBC** | Egress through locked doors | Sensor release, REX, fire-alarm release, no-delay rules |
| **ADA / ABA §404** | Accessibility | 5 lbf opening force, one-hand hardware, closing speed |
| **OSHA 1910.36** | Workplace exit routes | Exit doors must be unlocked from inside |

## The Author's Take

**Position:** In my view, the access-control cluster is where a locksmith or integrator is most likely to create a *code violation by accident* — because the hardware is forgiving of mistakes right up until the day of a fire or a power failure.

**Reasoning:** First, fail-safe vs fail-secure is a fire-and-life-safety decision, not a technical preference — a fail-secure device on an egress door is a trapped-occupant liability. Second, the credential layer and the physical layer are often specified by two different people, so the "secure card, plain Wiegand wiring" gap is extremely common. Third, the engineering tables (holding force, static/dynamic strength, cycles) are what actually separate a security lock from a traffic-control toy, yet most buyers shop on brand and price alone.

**Disclosure:** This is my professional opinion based on the published standards and manufacturer data cited across this hub, not verified first-party testing.

## Related Hubs

- [Lock Technology](../technology/index.md) — the mechanical latch and cylinder mechanisms an electric strike releases
- [Standards & Compliance](../standards/index.md) — fire/code and grading standards that intersect with egress hardware
- [Vault & Safe](../vault/index.md) — UL 768 / electronic safe locks, a separate electronic-lock domain
