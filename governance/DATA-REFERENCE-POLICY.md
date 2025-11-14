# DATA-REFERENCE-POLICY.md  
MaMeeFarm™ — Official Data Reference & Platform Deprecation Policy  
Version 1.1 — Effective Immediately  

---

## 1. Purpose

This document defines how MaMeeFarm™ manages **external data references** across:

- Proof-of-Life (PoL) records  
- NFT metadata (e.g., OpenSea, IPFS-based metadata)  
- GitHub repositories and verification logs  

The purpose is to ensure that MaMeeFarm™ data is:

- **Professionally governed**  
- **Legally defensible**  
- **Technically verifiable**  
- **Independent from emotional, short-lived platforms**  

MaMeeFarm™ is not “creating content for entertainment”; it is **producing verifiable data** for:

- AI training and analysis  
- Auditable digital assets  
- Long-term economic and legal use cases  

Because of this, MaMeeFarm™ must separate:

> **“Emotion-driven attention platforms”**  
> from  
> **“Evidence-grade data infrastructure.”**

---

## 2. Scope

This policy applies to:

- All NFT collections under MaMeeFarm™ (e.g., *7 Ducks of Hope*, *Seed of Hope*, Proof-of-Life series, future collections).  
- All metadata templates, JSON files, and generation scripts used for minting.  
- All references embedded in `external_url`, `description`, and related metadata fields.  
- All governance and documentation inside MaMeeFarm™ GitHub repositories.

This policy does **not** regulate how individuals use social media personally.  
However, it **does** define what is considered **“official data reference”** for MaMeeFarm™.

---

## 3. Strategic Position: Data vs. Emotional Platforms

MaMeeFarm™ recognizes that platforms like TikTok are:

- Designed for **emotional engagement**, virality, and short-term attention.  
- Governed by **opaque algorithms** and business interests that can change at any time.  
- Focused on **“how people feel”**, not on **“how data is structured, verified, and preserved.”**

MaMeeFarm™, in contrast, exists to create:

- **Stable, time-series Proof-of-Life data**  
- **Traceable, cryptographically-verifiable records**  
- **Infrastructure that AI, governments, and institutions can rely on for decades**

Therefore:

> TikTok is a **“field of emotion”** (emotion arena)  
> MaMeeFarm™ is a **“field of evidence and data”**

They are **not the same layer** and **cannot share the same governance rules**.

---

## 4. Rationale for Deprecating TikTok as a Data Source

MaMeeFarm™ will **not** use TikTok as a primary data reference nor embed TikTok links in metadata, for the following reasons:

### 4.1 Platform Volatility and Control

- Content can be removed, muted, shadow-banned, or restricted without prior notice.  
- The platform’s priority is **engagement and profit**, not **data integrity or verifiability**.  
- Access to historical content is ultimately controlled by a private company, not by MaMeeFarm™.

**Conclusion:** TikTok is **not suitable** as an anchor for long-term, high-value data.

---

### 4.2 Emotional Layer vs. Evidence Layer

- TikTok optimizes for **emotion, speed, reaction**, and **drama dynamics**.  
- MaMeeFarm™ optimizes for **truth, continuity, provenance**, and **auditability**.  
- Emotional narratives can coexist, but they **must not** be the **foundation** of a global Proof-of-Life data system.

**Conclusion:** Emotional platforms may be used (optionally) for awareness,  
but **they are out of scope** for **core data governance**.

---

### 4.3 Legal, Compliance, and AI-Readiness

- Institutions, regulators, and AI systems require **stable, referenceable, structured data**.  
- A TikTok link is **not a reliable legal reference** in a dispute, audit, or due-diligence process.  
- AI models that analyze MaMeeFarm™ need **clean URLs, consistent schemas, and long-term availability**, not broken embeds or deleted videos.

**Conclusion:** For legal and AI use, MaMeeFarm™ must stand on:

- **GitHub** (data authority, hash, lineage)  
- **Blockchain** (timestamp, immutability)  
- **MaMeeFarm.com** (human-readable narrative archive)

---

### 4.4 Independence and Sovereignty of Data

- If MaMeeFarm™ depends on TikTok for proof, then MaMeeFarm’s IP is indirectly controlled by a third party.  
- MaMeeFarm™ is building a **Proof-of-Work Data System**, not a “channel” under a social-media company.  

**Conclusion:**  
To protect sovereignty over its data and IP, MaMeeFarm™ must be **independent from any one emotional platform**, starting with TikTok.

---

## 5. Policy Statement

Effective immediately:

1. **TikTok and similar short-video platforms are deprecated as official data sources**  
   - No TikTok URL will be used as a canonical reference in metadata.  
   - No TikTok link will be embedded in `external_url` or similar metadata fields.

2. **MaMeeFarm.com is the primary human-readable data reference**  
   All official metadata must use:

   ```json
   "external_url": "https://www.mameefarm.com"
