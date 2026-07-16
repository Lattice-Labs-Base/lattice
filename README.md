# <img src="./IMG_3785.jpeg" width="80" valign="middle"> LATTICE ($LAT)

LATTICE is a decentralized verification infrastructure designed to protect the Base ecosystem against quantum computation threats through the modular VERA Protocol.

### 🌐 Official Links
- **Website:** [https://lattice-labs-base.github.io/lattice/](https://lattice-labs-base.github.io/lattice/)
- **Telegram:** [t.me/Lattice_LAT](https://t.me/Lattice_LAT)
- **BaseScan (Mainnet Asset Layer):** [View on BaseScan](https://basescan.org/token/0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74)

### 📊 Project Status
- **Current Core Phase:** Phase 2: PoC Validated & Anchor Verification
- **Asset Settlement:** Base Mainnet ($LAT Token Layer)
- **Verification Engine:** Render (Go ML-DSA-87 Backend)
- **Blockchain Anchor:** Base Sepolia (PQC Testnet PoC)
- **Security & Integrity:** Production-Oriented Core Architecture (Proprietary Middleware Engine with Public Anchor Verification)
- **LAT Token Contract:** `0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74`
- **VERA Anchor Contract (Base Sepolia):** `0x3915f1CAb29C890b6627a6AB28fBE13760A24cd6`

---

### 🚀 VERA Sandbox Terminal (Live Proof of Concept)
Experience our live end-to-end post-quantum cryptographic verification Proof of Concept (PoC). The terminal demonstrates how standard EVM user pipelines sync with a native ML-DSA-87 backend engine, anchoring cryptographic parameters directly onto the Base Sepolia blockspace.
👉 [Live Demo Sandbox Website](https://lattice-labs-base.github.io/lattice/)
👉 [Launch Sandbox DApp (Vercel)](https://vera-sandbox.vercel.app/)

### 🛡️ Core Architecture & Technical Workflow
The VERA Protocol utilizes a dual-key routing topology that decouples standard ledger authorization from quantum-safe proof anchoring, enforcing "Extend, not Replace" integration:

1. **Identity & Connectivity (CONNECT)**: Intercepts standard Web3 pipeline payloads from user interactions. Detects network parity on Base Sepolia (Chain ID: `0x14A34`).
2. **Lattice Payload Computation (SECURE)**: The secure backend performs native ML-DSA-87 signing and verification using lattice-based cryptographic primitives based on the ML-DSA algorithm standardized in NIST FIPS 204.
3. **On-Chain State Anchoring (VERIFY)**: Executes state commitment anchoring via the commitProof method, permanently recording data integrity permanence inside the Base Sepolia ledger.

---

### 🪙 Tokenomics & $LAT Utility
The **$LAT Token** serves as the core baseline economic asset governing and securing the post-quantum validation ecosystem:

* **Validator Staking Requirements**: Independent nodes running off-chain Verifier clusters will be required to lock a predetermined allocation of $LAT tokens as collateral. Malicious actions, prolonged downtime, or incorrect proof validation results in capital slashing.
* **Verification Fee Architecture**: Applications and external protocols requesting decentralized quantum-resistant state security coverage will bundle protocol interaction premiums denominated in $LAT, driving sustainable organic asset demand.

---

### 🗺️ Strategic Roadmap & Milestones

#### 🟩 Phase 1: Research & Architecture (Completed)
- Comprehensive mathematical formulation and system design of lattice-based post-quantum cryptography extensions compatible with EVM network layer rules.

#### 🟦 Phase 2: VERA Sandbox & Proof Anchoring (Completed)
- Execution of a fully functional, end-to-end working Proof of Concept (PoC).
- Successful deployment of the on-chain contract anchor on Base Sepolia.
- Integration of a native ML-DSA-87 secure backend middleware suite syncing wallet-to-blockchain latency pipelines.

#### 🟨 Phase 3: PQC SDK & Middleware Foundation (In Progress)
- Transitioning the core validation pipeline into production-ready developer components:
  - **SDK Foundation**: Modular libraries for rapid multi-platform integration.
  - **Payload Builder**: Automating off-chain lattice structure compilation.
  - **Verification API**: Streamlined endpoints for developer-ready middleware communications.

#### 🟥 Phase 4: Mainnet Readiness & Ecosystem Adoption (Planned Target)
- Deployment of optimized production contract anchors onto the Base Mainnet.
- Public release of stable developer toolkits under managed access control.
- Strategic onboarding of external decentralized applications (dApps) to build a primary PQC validation network infrastructure across the EVM ecosystem.

Implementation details may evolve as the protocol matures. Public documentation describes the protocol architecture and interfaces, while selected implementation details remain proprietary.

---

### ⚙️ VERA Payload Builder (PQC Engine Specs)

This section provides the technical integration specifications for the **VERA Payload Builder (Go-based PQC Engine)**, which serves as the core cryptographic backend for Phase 3.

#### 🌐 Active API Endpoints
These are backend API endpoints designed to receive structured JSON payloads. Accessing the frontend endpoint directly in a browser will return a 404 Not Found.

- **Frontend API (Vercel Endpoint):** `https://vera-payload-builder.vercel.app/api/test-sign`
- **PQC Backend (Render Engine):** Protected under internal network routing and secure access controls.

#### 🔒 Security & Key Management
- Cryptographic secrets are securely managed through encrypted environment configuration inside Render's administration panel and are never exposed in the public repository.

#### 🔌 API Specifications

##### **PQC Generation & Verification Pipeline (POST /api/test-sign)**
Triggers the end-to-end verification process, converting standard payload inputs into a secure, Go-calculated signature on the Render engine.

###### **Request Payload (Example Fields)**
- **algorithmId**: Integer (representing the selected quantum-safe signature scheme)
- **userAddress**: String (EVM-compatible wallet address, e.g., "0x...")
- **proofHash**: String (transaction or proof state hash, e.g., "0x...")

###### **Expected Response (200 OK)**
- **success**: true
- **message**: "Render Go-based ML-DSA PQC Engine processed successfully."
- **verification**: Valid (true), Method ("render_go_mldsa_87_verify")
- **data**: Contains the calculated payload (algorithmId, publicKeyHash, proofHash, userAddress, expiry, timestamp) and the computed signature.

#### 🛠️ Local Build & Deployment Commands

##### **Render (Go Runtime)**
- **Build Command:** `go build -o main api/main.go api/pqc_engine.go`
- **Start Command:** `./main`

---
© 2026 Lattice Labs. All rights reserved. Some implementation details remain proprietary.
