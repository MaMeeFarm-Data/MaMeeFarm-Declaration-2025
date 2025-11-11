# 🔐 Checksum & Verification Guide  
### MaMeeFarm™ Proof-of-Work Data System — GitHub Verification Standard  

---

## 1️⃣ Purpose  

This document defines how **MaMeeFarm™** verifies, validates, and protects the integrity of every dataset, NFT proof, and record inside the repository. All verification uses **GitHub commit hashes** as the primary layer of proof and **SHA-256 checksums** as the secondary layer for cross-audit.

> “Every commit is proof of real work. Every hash is the fingerprint of truth.”

---

## 2️⃣ Verification via GitHub Commit  

GitHub automatically generates a **unique commit hash** for every file update. Each commit contains the file’s full history, author identity, and timestamp — creating an immutable audit trail recognized globally.

### ✅ Example Record
file: valuation/MMFARM-IP-Statement-2025.md  
commit: 5cee7ec7f9a48f2e67bde1a2aeb4a4f5f35d97af  
author: MaMeeFarm-Data  
verified_at: 2025-11-11T04:17:00Z  
status: ✅ Verified via GitHub Commit  

**Steps to verify:**  
1. Open the file on GitHub.  
2. Click **“History”** to view its commit list.  
3. Select the commit ID and confirm author + timestamp.  
4. Record the commit hash and date in `governance/integrity-proof.sha256`.

---

## 3️⃣ Cross-Verification Using SHA-256  

While the GitHub commit hash ensures authorship and time integrity, SHA-256 provides a file-level fingerprint that guarantees content immutability for ISO, WIPO, or blockchain-level audits.

### 🧮 Generate a SHA-256 Checksum  

**Linux / macOS**  
shasum -a 256 <path/to/file>  

**Windows PowerShell**  
Get-FileHash -Algorithm SHA256 <path\to\file>  

### ✅ Example Output  
3b1a98d5c1b4e6d44e32efb94d8b5a32e25f67f09df29a3b8e13e6239a10a6c9  

**Record the result in:**  
- `governance/integrity-proof.sha256`  
- `registry/collection-proof/proof-index.json`

---

## 4️⃣ Verification Workflow  

| Step | Action | Output |
|------|---------|---------|
| 1️⃣ | Commit the file to GitHub | Creates immutable record |
| 2️⃣ | Compute SHA-256 locally | Confirms content integrity |
| 3️⃣ | Record both hash + commit | In `integrity-proof.sha256` |
| 4️⃣ | (Optional) Anchor to Polygon | Adds blockchain timestamp |
| 5️⃣ | Cross-verify with registry | Confirms proof consistency |

---

## 5️⃣ Example Unified Entry  

file: registry/collection-proof/proof-7-ducks-of-hope.md  
commit: e1a473f54c2c6b58a12f90c7cd1139a6b2fadb45  
sha256: 9a47b49d2e5f79b4d3f431b02bb93ce8a6c54b16b3a07c8738b172932937f2a8  
verified_at: 2025-11-11T08:00:00Z  
status: ✅ Verified  

---

## 6️⃣ Automation (Optional GitHub Action)  

When ready, add a workflow file at `.github/workflows/verify-integrity.yml` to automate checksum validation for every commit.

name: Verify Integrity  
on: [push, pull_request]  
jobs:  
  verify:  
    runs-on: ubuntu-latest  
    steps:  
      - uses: actions/checkout@v4  
      - name: Compute SHA-256  
        run: |  
          echo "🔍 Checking MaMeeFarm™ proofs..."  
          shasum -a 256 registry/collection-proof/*.md valuation/*.md > sha256_output.txt  
      - name: Display Results  
        run: cat sha256_output.txt  

---

## 7️⃣ Contact  

📧 governance@mameefarm.com *(Placeholder – pending official setup)*  
🌐 https://www.mameefarm.com  

---

© 2025 **MaMeeFarm™** — Proof-of-Work Farm Data System  
Licensed under **MMFARM-POL-2025 + CC BY-NC 4.0 Overlay**

---

