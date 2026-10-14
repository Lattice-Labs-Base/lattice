# <img src="./IMG_3785.jpeg" width="80" valign="middle"> LATTICE ($LAT)

LATTICE is a decentralized verification infrastructure designed to protect the Base ecosystem against quantum computation threats through the modular VERA Protocol.

### 🌐 Official Links
- **Website:** [https://lattice-labs-base.github.io/lattice/](https://lattice-labs-base.github.io/lattice/)
- **Telegram:** t.me/Lattice_LAT
- **BaseScan (Mainnet Asset Layer):** [https://basescan.org/token/0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74](https://basescan.org/token/0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74)
- **Live Terminal DApp:** [https://vera-sdk-mainnet.vercel.app/](https://vera-sdk-mainnet.vercel.app/)
- **SDK JavaScript Distribution:** [https://vera-sdk-mainnet.vercel.app/vera-pqc-sdk.js](https://vera-sdk-mainnet.vercel.app/vera-pqc-sdk.js)

### 📊 Project Status
- **Current Core Phase:** Phase 4: Production Mainnet Deployment & Commercialization Transition
- **Asset Settlement:** Base Mainnet ($LAT Token Layer)
- **Verification Engine:** Go-based ML-DSA-87 Engine (Render Microservice)
- **Blockchain Anchor:** Base Mainnet
- **Security & Integrity:** Production-Oriented Post-Quantum Anchoring Architecture
- **LAT Token Contract:** `0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74`
- **VERA Anchor Contract (Base Mainnet V5):** `0x34233747E842082fCfeAC2f248159EcB4a6c6f04`

---

### 🏗️ System Architecture

<pre><code>  [ Web3 Wallet / External DApp ]
                 │
                 ▼
  [ VERA PQC Client SDK / Terminal ]
                 │
                 ▼
     [ Vercel Routing Layer ]
                 │
                 ▼
   [ Go PQC Engine (Render Node) ]
   (ML-DSA-87 / NIST FIPS 204)
                 │
                 ▼
   [ Base Mainnet Anchor Contract ]
  (0x3423...6f04 / commitProof)</code></pre>

---

### 🚀 VERA Terminal & Client Integration

VERA Protocol provides both a live interactive terminal and an integrable JavaScript SDK (`vera-pqc-sdk.js`) for Web3 application developers to secure EVM workflows against post-quantum threats.

#### ⚡ 1. One-Line SDK Integration
Developers can integrate post-quantum proof generation and Base Mainnet anchoring directly into their HTML/JS application:

<pre><code>&lt;!-- Ethers.js Dependency --&gt;
&lt;script src="https://cdnjs.cloudflare.com/ajax/libs/ethers/5.7.2/ethers.umd.min.js"&gt;&lt;/script&gt;

&lt;!-- VERA PQC SDK --&gt;
&lt;script src="https://vera-sdk-mainnet.vercel.app/vera-pqc-sdk.js"&gt;&lt;/script&gt;

&lt;script&gt;
  // Initialize SDK
  const vera = new VeraSDK();

  async function runPQC() {
    try {
      // Step 1: Connect, generate ML-DSA-87 proof, and commit anchor to Base Mainnet in one call
      const result = await vera.anchor(window.ethereum);
      
      console.log("Transaction Hash:", result.transactionHash);
      console.log("BaseScan URL:", result.scanUrl);
    } catch (error) {
      console.error("PQC Anchoring Failed:", error);
    }
  }
&lt;/script&gt;</code></pre>

#### 🖥️ 2. Sandbox Terminal
- **Live Terminal DApp:** https://vera-sdk-mainnet.vercel.app/
- **Official Portal:** https://lattice-labs-base.github.io/lattice/

---

### 🛡️ Core Architecture & Technical Workflow

The VERA Protocol utilizes a dual-key routing topology that decouples standard ledger authorization from quantum-safe proof anchoring, enforcing an "Extend, not Replace" integration paradigm:

1. **Identity & Connectivity (CONNECT)**: Intercepts Web3 provider payloads and ensures chain alignment with Base Mainnet (Chain ID: `0x2105` / `8453`).
2. **Lattice Payload Computation (SECURE)**: The high-performance Go backend executes native ML-DSA-87 (Dilithium) signing based on NIST FIPS 204 post-quantum standards.
3. **On-Chain State Anchoring (VERIFY)**: Automatically commits the generated proof state hash to the `VERA_Protocol_V5_0` contract on Base Mainnet (`commitProof`), providing sub-cent transaction anchoring proof immutability.

---

### 🪙 Ecosystem & $LAT Economic Model

The **$LAT token** (`0x0a320C8daC9fB56C7FC766CDF2c6068949fa4B74`) is the primary value-capture and governance asset powering the Lattice ecosystem.

#### 🔑 Progressive Integration Strategy
- **Phase 1 (Current): Open Developer Onboarding**: VERA currently provides open, friction-free verification so developers can seamlessly integrate and test post-quantum security without initial token friction.
- **Phase 2 (Planned): Commercialization & Revenue Generation**: VERA will introduce tiered commercial API models, usage-based verification fees for high-volume dApps, and enterprise SLA support.

#### 🎯 Core $LAT Value Capture & Revenue Allocation
1. **Systematic Revenue Reinvestment (Planned)**:
   - Net protocol revenues generated through commercial VERA offerings (such as API subscriptions, usage tiers, or enterprise integration services)—after operational infrastructure costs—will be **systematically reinvested back into the ecosystem**.
   - Funds will be strategically allocated to **deepen and reinforce $LAT liquidity pools, drive developer adoption through marketing & ecosystem grants, and support ongoing protocol R&D**.
   - This ensures that commercial VERA growth directly strengthens $LAT market depth, liquidity stability, and overall ecosystem footprint.
2. **Community Governance**:
   - Holding $LAT grants voting power on protocol parameters, Treasury allocations, grant distribution, and commercial fee structures.
3. **Future Deflationary & Staking Evaluation (R&D)**:
   - As the protocol reaches sustainable scale, the rollout of a targeted **$LAT Buyback & Burn mechanism** and **decentralized verifier node staking** will be evaluated based on network maturity and liquidity depth.

---

### 🗺️ Strategic Roadmap & Milestones

#### 🟩 Phase 1: Research & Architecture ✔ Completed
- Mathematical design and system architecture of EVM-compatible lattice-based cryptography.

#### 🟦 Phase 2: VERA Sandbox & Testnet Anchoring ✔ Completed
- Successful execution of testnet Proof of Concept (PoC) on Base Sepolia.
- Deployment and testing of internal Go-based proof computation microservices.

#### 🟨 Phase 3: PQC SDK & Mainnet Foundation ✔ Completed
- Production-ready Go microservice deployment supporting ML-DSA-87 / NIST FIPS 204 algorithms.
- Release of `vera-pqc-sdk.js` and live Base Mainnet anchor contract deployment (`0x3423...6f04`).

#### 🟥 Phase 4: Mainnet Ecosystem Adoption & Commercial Transition (Active)
- **✔ Completed:** Live End-to-End production pipeline (Vercel DApp ⇔ Render Go Engine ⇔ Base Mainnet EVM).
- **In Progress:** Onboarding Base ecosystem dApps through the free developer verification tier.
- **Planned:** Rollout of commercial API subscription tiers and execution of the **$LAT Revenue Reinvestment Program**.

---

### ⚙️ Smart Contract Reference (Base Mainnet)

- **Network:** Base Mainnet (Chain ID: `8453` / `0x2105`)
- **Contract Address:** [`0x34233747E842082fCfeAC2f248159EcB4a6c6f04`](https://basescan.org/address/0x34233747E842082fCfeAC2f248159EcB4a6c6f04)
- **Core Interface:** `commitProof(string requestId, address userAddress, string proofHash, string polyMapping)`

---
© 2026 Lattice Labs. All rights reserved. Selected implementation details remain proprietary.
