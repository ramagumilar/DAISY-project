# DAISY (Decentralized Authentication Identity System) - Proof of Concept


## Overview
DAISY is a decentralized authentication and identity verification system built on blockchain. It allows users to register schemas, verify identities, and submit proofs (Blob IDs) integrated with the Soundness Layer.


## Architecture
The DAISY PoC consists of:
- **Frontend (React):** User interface for schema registration, verification, and proof submission.
- **Smart Contracts:** On-chain registry and verifier contracts.
- **Soundness Layer Integration:** For proof verification.
- **Optional Backend:** Automates Blob ID submission.
- **Decentralized Storage (e.g., IPFS):** For storing proof data.


### Architecture Diagram
![DAISY Architecture].<img width="1536" height="1024" alt="daisy" src="https://github.com/user-attachments/assets/e8e59abf-8c19-4e7d-91e6-ef440a250d2c" />




## Features
- Register and manage schemas on-chain.
- Verify user identities via smart contracts.
- Submit and verify proofs (Blob IDs) with Soundness Layer.
- Decentralized storage support.


## Installation
1. Clone the repository.
2. Install dependencies: `npm install`
3. Start local blockchain (Hardhat): `npx hardhat node`
4. Deploy contracts: `npx hardhat run scripts/deploy.js --network localhost`
5. Run frontend: `npm start`


## Usage
- Connect wallet.
- Register a new schema.

- Verify identities.
- Submit Blob ID manually or via backend automation.


## Collaboration & Permissions
For any collaboration inquiries or permission to contribute/edit this project, please contact:
**ramagumilar9@gmail.com*


Unauthorized copying or imitation of this project is prohibited.


---
