# 🗳️ Decentralized Voting DApp  
### Solidity | Next.js | Hardhat | IPFS (Pinata)

A secure and transparent blockchain-based voting application built using **Solidity smart contracts**, **Hardhat**, and **Next.js**.

This system eliminates centralized control and ensures tamper-proof voting using Ethereum blockchain technology.

---

# 📌 Problem Statement

Traditional voting systems can suffer from:

- Centralized authority control  
- Risk of data manipulation  
- Lack of transparency  
- Security vulnerabilities  

This project solves these issues using blockchain technology to ensure transparency, immutability, and decentralization.

---

# 🚀 Key Features

- ✅ Decentralized voting using Ethereum  
- ✅ Smart contract-based voting logic  
- ✅ Secure voter & candidate registration  
- ✅ Voting period control  
- ✅ Automatic winner calculation  
- ✅ IPFS storage using Pinata  
- ✅ MetaMask wallet integration  
- ✅ Admin approval system  

---

# 🖼️ Application Screenshots

## 🏠 Home Page

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/Homepage.png" width="900"/>

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/Candi_reg.png" width="900"/>

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/voter_reg.png" width="900"/>

---

## 🗳️ Voting Dashboard

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/candiatates.png" width="900"/>

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/Screenshot%20(26).png" width="900"/>

---

## 📊 Admin Dashboard

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/Screenshot%20(24).png" width="900"/>

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/approval.png" width="900"/>

---

## 🏆 Winner Page

<img src="https://raw.githubusercontent.com/benherr/MAINPROJECT/main/voting-dapp/Images/winnerPage.png" width="900"/>

The winner page automatically displays the candidate with the highest votes after the voting period ends.

---

# 🏗️ System Architecture

```text
User
  │
  ▼
Next.js Frontend
  │
  ▼
Smart Contract (Solidity)
  │
  ▼
Ethereum Blockchain
  │
  └──────────────► IPFS Storage (Pinata)
```

---

# 📦 IPFS Storage Using Pinata

## 📦 Pinata Dashboard

<img src="https://github.com/benherr/MAINPROJECT/blob/main/voting-dapp/Images/pinnata.png" width="900"/>

---
## 📌 Why Pinata?

- Reliable IPFS pinning service  
- Ensures permanent file availability  
- Easy API integration  
- Secure API key authentication  

---

## 🔄 How It Works

1. User uploads candidate image or document  
2. File is sent to Pinata API  
3. Pinata stores file on IPFS  
4. IPFS hash (CID) is returned  
5. CID is stored inside the smart contract  
6. File is retrieved using:

```text
https://gateway.pinata.cloud/ipfs/<CID>
```

---

## 📊 Pinata File Flow Diagram

```text
User Upload
     │
     ▼
Frontend (Next.js)
     │
     ▼
Pinata API
     │
     ▼
IPFS Network
     │
     ▼
Returns CID
     │
     ▼
Stored in Smart Contract (Solidity)
```

---

# 📜 Smart Contract Details

- Written in Solidity ^0.8.x  
- Developed & tested using Hardhat  
- Stores:
  - Candidate details  
  - Vote counts  
  - IPFS CID  
- Implements:
  - Voting period restriction  
  - Candidate approval system  
  - getWinningCandidate() logic  
  - Access control  

---

# 🔐 Security Considerations

- Immutable vote storage on blockchain  
- Voting allowed only during active period  
- Admin approval before candidate listing  
- IPFS CID stored on-chain for integrity  
- API keys stored in environment variables  
- MetaMask-based authentication  

---

# ⚙️ Prerequisites

- Node.js v18+  
- Hardhat  
- MetaMask browser extension  
- Pinata account  

---

# 🚀 Installation & Setup

```bash
# Clone repository
git clone https://github.com/benherr/MAINPROJECT.git

# Navigate to project
cd voting-dapp

# Install dependencies
npm install

# Run development server
npm run dev
```

Make sure MetaMask is connected to your local Hardhat network or testnet.

---

# 📁 Project Structure

```text
voting-dapp/
│
├── contracts/
├── pages/
├── components/
├── context/
├── Images/
├── hardhat.config.js
└── package.json
```

---

# 📦 Key Dependencies

- Next.js  
- React  
- Hardhat  
- Web3Modal  
- Axios  
- React Dropzone  

---

## 🌐 Deployment

Currently deployed on local Hardhat network.
Can be deployed to:
- Polygon Testnet
- Ethereum Sepolia


📖 Detailed deployment instructions available here:

👉 [View Deployment Guide](./DEPLOYMENT.md)
---





---

⭐ If you like this project, give it a star!
