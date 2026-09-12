---
title: "Access Control Credentials Explained: 125kHz Prox, 13.56MHz MIFARE/DESFire, Seos, Mobile, UHF — and the Wiegand vs OSDP Divide"
description: "Access control credentials compared by frequency, encryption, and migration path: 125kHz prox vs 13.56MHz MIFARE Classic/DESFire vs HID Seos vs mobile vs UHF — plus why Wiegand is a protocol, not a card, and why OSDP replaces it."
---
# Access Control Credentials Explained: Prox, Smart Cards, Seos, Mobile, UHF — and the Wiegand vs OSDP Divide

> 项目：Locktool · Content
> 类型：Access Control Cluster（模板 G/H）
> 所属 Hub：Access Control Hub（/access-control/）
> 主实体：`https://locktool.com/entity/credential#entity`、`https://locktool.com/entity/prox-card#entity`、`https://locktool.com/entity/smart-card#entity`、`https://locktool.com/entity/wiegand#entity`、`https://locktool.com/entity/osdp#entity`
> 状态：UPGRADED v0.2
> 研究日期：2026-09-12

---

## Quick Answer

A credential is the thing that proves identity to the reader. The **security dividing line is encryption**: 125kHz prox cards and 13.56MHz MIFARE Classic transmit data that can be read and reproduced; MIFARE DESFire (EV1/EV2/EV3), HID Seos, and modern mobile credentials use AES/3DES with mutual authentication and are the current high-assurance options. The reader-to-controller wire matters just as much — **Wiegand is an unencrypted one-way interface, while OSDP adds encryption, supervision, and two-way control.**

> **Definition — Credential:** any token (card, fob, phone, PIN, or biometric) that a reader presents to the controller as proof of identity for an access decision. The credential's *technology* (frequency, memory, cryptography) — not its physical shape — determines its resistance to duplication.

## The Credential Landscape at a Glance

| Credential | Frequency | Encryption / auth | Read range (typical) | Duplication resistance |
|---|---|---|---|---|
| PIN / keypad | — | None (shared secret) | Contact | Low (observable/shareable) |
| Magstripe | — | None | Swipe | Low |
| **125kHz Prox** | 125 kHz (LF) | None — fixed ID in clear | ~2–6 in | Low |
| **MIFARE Classic** | 13.56 MHz (HF) | Proprietary CRYPTO1 (broken) | ~up to 4 in (ISO 14443) | Low–medium |
| **MIFARE DESFire EV1/2/3** | 13.56 MHz (HF) | AES-128 + 3DES, mutual auth | ~up to 4 in (ISO 14443) | High |
| **HID Seos / iCLASS SE** | 13.56 MHz (HF) | AES-128, mutual auth | ~up to 4 in (ISO 14443) | High |
| **Mobile credential** | NFC / BLE | AES-128 (Seos on phone) | NFC ~inches; BLE ~feet | High |
| **UHF (long-range)** | 860–960 MHz | Varies by implementation | Several meters (up to ~15 m) | Varies |
| **Biometric** | — | Template match | Contact/near | High (but non-revocable) |

## The Prox Card: Legacy, Ubiquitous, and Inherently Insecure

125kHz proximity cards remain "the most widely used card for electronic access in North America" (ColorID [F]), but they carry a structural weakness that no firmware patch fixes:

- The chip holds **only a fixed identifier** — typically a **facility code + card number** — and transmits it **in the clear** when energized by the reader field. There is **no cryptographic check** that the card is genuine.
- Because the data is a static, unencrypted ID, a prox credential is **vulnerable to duplication** — the ID is read in the clear and can be reproduced. This is a documented, industry-acknowledged risk — the reason the industry has been migrating away for two decades.
- Prox cards also **can't store applications** (no memory for multiple functions), so they're a door-access-only token.

**Why it still exists:** backward compatibility. Facilities with thousands of prox cards and readers keep it running because a forklift migration is expensive — not because prox is secure.

## 13.56MHz Smart Cards: MIFARE Classic vs DESFire

Both operate at 13.56MHz, but they are **a generation apart** in security:

| | MIFARE Classic | MIFARE DESFire EV1/EV2/EV3 |
|---|---|---|
| Introduced | Mid-1990s | 2006 onward (EV1) |
| Crypto | Proprietary **CRYPTO1** cipher | Open **AES-128 + 3DES** |
| Auth | Mutual auth (but cipher is broken) | Mutual auth, secure key storage |
| Memory | Fixed sectors | Flexible secure file system |
| Multi-application | Limited | Yes (access + payment + transit + ID) |
| NFC compatibility | Partial | Full NFC |
| Duplication resistance | **Compromised** (cipher cryptographically broken) | **High** — not publicly broken |

The key correction to internalize: **MIFARE Classic's CRYPTO1 cipher has been cryptographically broken**, so Classic cards are *more* secure than prox but still **vulnerable to duplication** by specialized equipment. **DESFire** uses well-vetted, publicly scrutinized AES/3DES on a secure microcontroller, which is why it's the enterprise/multi-application default (RFIDCard / ColorID [F]).

**Read-range note:** ISO 14443 (MIFARE/Seos/iCLASS) cards read up to ~10 cm (4 in); ISO 15693 HF cards read a few inches to about a foot (Telaeris [F]). Neither is a "long-range" credential.

## HID Seos and iCLASS SE: The High-Assurance Tier

- **HID Seos** is a software-based credential using **AES-128 encryption and mutual authentication** between credential and reader; HID states it is the first finished access-control card certified by independent lab **TÜV** (HID Global [F]).
- **iCLASS SE** wraps credential data in a **Secure Identity Object (SIO)** for 13.56MHz cards.
- Seos is deliberately **multi-application** — access, secure printing, cashless vending, network login — and it is the technology behind HID's **mobile credentials**.

## Mobile Credentials (NFC / BLE)

A mobile credential puts the same secure technology (e.g., Seos) onto a phone, delivered via an app or wallet, then presented over **NFC or BLE** (HID Mobile Access [F]). The advantages: instant remote issuance/revocation, no physical card to lose, and the credential lives inside the phone's secure element. The trade-offs: dependency on the phone's battery and OS, and a different (longer, BLE) read interaction than a card tap.

## UHF Long-Range: For Vehicles and Gates, Not Doors

UHF RFID (860–960 MHz) is the long-range layer for **vehicle/gate access, parking, and perimeter** identification — windshield tags and passive tags read at **several meters, up to ~15 m** on high-end readers (Nedap TRANSIT [F]). It is **not** the right tool for pedestrian doors (you don't want a door unlocking from 5 meters away), and its security varies by implementation — so long-range vehicle credentials should be evaluated the same way as any other: on encryption, authentication, and revocation, not on read range alone.

## Wiegand vs OSDP: The Wire Is Part of the Security Model

The biggest terminology error in access control is calling "Wiegand" a card. It is an **interface standard** — the electrical/protocol link between reader and controller.

**Wiegand (legacy interface):**

- **One-way** — the reader sends data to the controller; the controller can't talk back or supervise the reader.
- **Unencrypted** — credential data travels in the clear on the wire; if the wiring is physically accessed, data can potentially be intercepted (Axis [F]).
- **Classic "26-bit" format** — facility code + card number + parity bits; more bits = larger ID space, but more bits don't add encryption.
- **~500 ft (150 m)** practical cable distance, and readers need extra wires for LED/buzzer/tamper.

**OSDP (Open Supervised Device Protocol, SIA):**

- **Two-way** over RS-485 — the controller supervises, configures, and detects tampering/replacement of the reader.
- **AES-128 "Secure Channel"** — encrypts reader-to-controller traffic, closing the plaintext gap Wiegand leaves open.
- **~4,000 ft** runs and **multi-drop** (multiple readers on one connection).
- Standardized by the **Security Industry Association** and adopted as an **IEC international standard** (Axis/SIA [F]).

**The takeaway:** a DESFire or Seos card on a Wiegand reader is still transmitting over an unencrypted, unsupervised wire. **"Secure credential" and "secure transport" are two separate decisions** — the card protects the credential; OSDP protects the wire.

## Selection Framework

| Your situation | Choose |
|---|---|
| Legacy system, thousands of prox cards, low-risk interior doors | Keep 125kHz prox (document the risk; plan migration) |
| Low-cost, low-risk interior door | PIN / keypad |
| Need encryption + one application, budget-conscious | MIFARE Classic — **only** if you accept its broken cipher |
| Need encryption + multi-application + future-proofing | MIFARE DESFire EV2/EV3 |
| Enterprise, mobile, or highest assurance | HID Seos / iCLASS SE (or equivalent AES credential) |
| Vehicle / gate / parking long-range | UHF (860–960 MHz) |
| Prevent sharing / "who you are" | Biometric — **as one factor of MFA**, never alone |
| Remote issuance, temporary visitors | Mobile credential (NFC/BLE) |
| New reader-to-controller wiring | **OSDP** (not Wiegand) |

## The Author's Take

**Position:** In my view, the credential is the most *over-trusted* layer in access control — organizations spend on encrypted cards and then wire them to readers over a plaintext Wiegand link, which is like putting a deadbolt on a door with an unlocked window.

**Reasoning:** First, the industry's own guidance shows 125kHz prox transmits a fixed, unencrypted ID and MIFARE Classic's cipher is cryptographically broken — so anything below DESFire/Seos-class should be treated as a known, documented risk, not a "good enough" default. Second, encryption only counts if it spans the whole path; Wiegand's unencrypted, unsupervised wire silently voids the benefit of an encrypted card, which is exactly why OSDP exists. Third, biometrics are powerful but **non-revocable** — a compromised fingerprint can't be rotated like a card, so biometrics belong as a second factor, not a standalone credential.

**Disclosure:** This is my professional opinion based on the credential-technology and protocol documentation cited below, not first-party testing or a vendor endorsement.

## FAQ

**Is Wiegand a type of card?**
No. Wiegand is the reader-to-controller **interface** (one-way, unencrypted). The classic "26-bit" is a data *format* on that interface, not a credential technology.

**Prox vs smart card — what's the real difference?**
Prox (125kHz) transmits a fixed, unencrypted ID and can't store applications. Smart cards (13.56MHz) have memory and cryptography — but the *level* depends on the chip: MIFARE Classic's cipher is broken; DESFire uses AES-128/3DES with mutual authentication.

**What does OSDP do that Wiegand can't?**
OSDP (SIA) is bidirectional over RS-485, adds AES-128 Secure Channel encryption, supervises the reader (tamper detection), supports ~4,000 ft runs and multi-drop. Wiegand is one-way, plaintext, and ~500 ft.

**Are biometrics the most secure credential?**
They're hard to lose and share, but a biometric template is **non-revocable** — once compromised it can't be reset like a card or PIN. Use biometrics as one factor of MFA in high-security settings.

**What's the migration path off prox?**
Issue **multi-technology cards** (e.g., Seos + prox, or DESFire + prox) so one badge works on both old and new readers, then replace readers/controllers to OSDP over time — the credential side moves first, the infrastructure follows.

## Sources

- ColorID — "MIFARE DESFire EV1 vs EV2": https://www.colorid.com/ev1-vs-ev2.html — 125kHz prox most widely used in NA; MIFARE Classic mid-1990s, cipher broken
- ASAP Identification — "Differences: Proximity, MIFARE, DESFire": https://www.asapident.com/differences-proximity-mifare-mifare-desfire — prox 26–60+ bit fixed ID; DESFire EV1/EV2 microprocessor
- RFIDCard — "MIFARE Classic vs DESFire": https://www.rfidcard.com/mifare-classic-vs-desfire-key-differences-security-applications-and-how-to-choose-the-right-rfid-card — DESFire AES-128/3DES
- HID Global — "HID Seos": https://www.hidglobal.com/product-mix/seos — AES-128, mutual authentication, TÜV certification
- HID Global — "HID Seos Card": https://www.hidglobal.com/products/seos-card — modern cryptography + mutual authentication
- Telaeris — "Understanding HID Security Card Types": https://telaeris.com/understanding-hid-security-card-types — ISO 15693 read range, ISO 14443 ~10 cm, mobile NFC/BLE
- Axis — "OSDP protocol in access control" (white paper): https://whitepapers.axis.com/en-us/osdp-protocol-in-access-control — Wiegand plaintext/one-way/500 ft; OSDP AES-128/bidirectional/RS-485/IEC
- SIA — "Open Supervised Device Protocol (OSDP)": https://www.securityindustry.org/industry-standards/open-supervised-device-protocol — OSDP purpose and scope
- Nedap Identification Systems — "Long Range RFID": https://www.nedapidentification.com/rfid/long-range-rfid — UHF vehicle identification, TRANSIT up to 15 m

> 研究日期：2026-09-12 · 访问日期：2026-09-12。以上均为第三方权威制造商/标准组织公开资料，非我方实测。本文仅讨论凭证的**原理、风险披露与合规选型**，不提供任何操作层面的进入方法。具体选型应结合真实威胁模型并由专业人员评估。

## 关联

- → [Electronic Access Control Explained](electronic-access-control-explained.md)（凭证→读卡器→控制器→锁具全栈，凭证是第 1–3 层）
- → [Electric Strike vs Maglock](electric-strike-vs-maglock.md)（凭证验证通过后的物理执行层）
- → [Lock Security Standards Explained](../standards/lock-security-standards-explained.md)（凭证/锁具相关标准全景）
- → [Safe Lock Types Explained](../vault/safe-lock-types-explained.md)（电子锁的另一安全域）
- → Entity：`https://locktool.com/entity/credential#entity` / `https://locktool.com/entity/prox-card#entity` / `https://locktool.com/entity/smart-card#entity` / `https://locktool.com/entity/wiegand#entity` / `https://locktool.com/entity/osdp#entity`
