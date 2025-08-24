# DAISY – Decentralized Authentication & Identity System

**DAISY** is a decentralized system for **schema registration, identity verification, and proof submission (Blob IDs)** built on **blockchain**.  
This version includes **Biometric KYC** (face/fingerprint) and **Soundness Layer** integration for secure and privacy-preserving cryptographic verification.

---

## 🏛️ Architecture

Main components of DAISY:

- **Frontend (React)**  
  User interface for schema registration, biometric capture, identity verification, and proof submission.

- **Smart Contracts (Solidity)**  
  Store schemas, biometric hashes, and provide on-chain verification functions.

- **Soundness Layer**  
  Zero-knowledge proof layer for validating biometric verification and Blob IDs.

- **Decentralized Storage (IPFS / Walrus Protocol)**  
  Stores encrypted proofs or biometric templates; never raw biometric data.  
  Walrus provides high-availability decentralized storage.

- **Optional Backend**  
  Automates Blob ID submission and may assist with biometric feature extraction.

---

### 🖼️ Architecture Diagram

DAISY Architecture <img width="1536" height="1024" alt="daisy" src="https://github.com/user-attachments/assets/a1763b9a-069b-4c20-925b-7fc14d1c4bba" />


---

## ✨ Features

- Register & manage **schemas** on-chain.  
- Verify identities through smart contracts.  
- **Submit & verify Blob IDs** via the Soundness Layer.  
- Support for **decentralized storage** (IPFS/Walrus Protocol).  
- **Biometric KYC**:
  - Enroll biometric data (face/fingerprint → hash).  
  - Verify biometric data via on-chain hash matching.  
  - Integrate proof verification with zk-proofs for privacy.  
- **Privacy-preserving**: no raw biometric data is stored.

---

## ⚡ Workflow

### 1. Enrollment
- User captures biometric data (face/fingerprint) via the frontend.  
- Data → processed into a **biometric hash**.  
- Hash stored in the smart contract.  

### 2. Verification
- User performs biometric scan again.  
- Frontend → sends new hash to the Soundness Layer.  
- Soundness Layer:  
  - Compares hash with the registered on-chain value.  
  - Generates a **zk-proof** to prove validity.  

### 3. Proof Submission
- The zk-proof is packaged as a **Blob ID**.  
- Blob ID submitted and verified on-chain.  
- Final result recorded in the blockchain.  

---

## 📦 Installation

```bash
git clone https://github.com/ramagumilar/DAISY-project.git
cd DAISY-project
npm install
npx hardhat node
npx hardhat run scripts/deploy.js --network localhost
npm start




🔐 Privacy & Security Notes

- No raw biometric data is stored, only hashed or encrypted templates.
- Use encryption (AES/RSA) when storing biometric templates in IPFS/Walrus.
- Soundness Layer + zk-proofs ensure privacy-preserving verification.
- Recommended: liveness detection to prevent spoofing attacks.

📚 Tech Stack

- React – Frontend UI.
- Hardhat – Smart contract development & local blockchain.
- Solidity – Smart contracts for schema, biometric, verification.
- IPFS / Walrus Protocol – Decentralized encrypted proof storage.
- face-api.js / WebAuthn – Biometric capture (face/fingerprint).
- circom / snarkjs – Zero-Knowledge Proof for biometrics.
