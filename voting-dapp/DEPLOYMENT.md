---

# 🌐 Deployment Guide (Sepolia / Polygon)

This project can be deployed to Ethereum Sepolia Testnet or Polygon Testnet using Hardhat.

---

## 🧰 Prerequisites

- MetaMask installed
- Testnet ETH or MATIC
- Alchemy / Infura RPC URL
- Private wallet key
- Etherscan / Polygonscan API key

---

# 🚀 Deploy to Ethereum Sepolia

## 1️⃣ Install Dependencies

```bash
npm install --save-dev @nomicfoundation/hardhat-toolbox dotenv
```

---

## 2️⃣ Configure `.env` File

Create a `.env` file in root directory:

```env
SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR_API_KEY
PRIVATE_KEY=YOUR_WALLET_PRIVATE_KEY
ETHERSCAN_API_KEY=YOUR_ETHERSCAN_API_KEY
```

⚠️ Never share your private key publicly.

---

## 3️⃣ Update `hardhat.config.js`

```javascript
require("@nomicfoundation/hardhat-toolbox");
require("dotenv").config();

module.exports = {
  solidity: "0.8.18",
  networks: {
    sepolia: {
      url: process.env.SEPOLIA_RPC_URL,
      accounts: [process.env.PRIVATE_KEY],
    },
  },
  etherscan: {
    apiKey: process.env.ETHERSCAN_API_KEY,
  },
};
```

---

## 4️⃣ Deploy Smart Contract

```bash
npx hardhat run scripts/deploy.js --network sepolia
```

After deployment, you will see:

```
Contract deployed to: 0xYourContractAddress
```

Save this address.

---

## 5️⃣ Verify Contract on Etherscan

```bash
npx hardhat verify --network sepolia DEPLOYED_CONTRACT_ADDRESS
```

View verified contract at:

```
https://sepolia.etherscan.io/address/YOUR_CONTRACT_ADDRESS
```

---

# 🚀 Deploy to Polygon (Amoy / Mumbai)

## 1️⃣ Update `.env`

```env
POLYGON_RPC_URL=https://polygon-amoy.g.alchemy.com/v2/YOUR_API_KEY
POLYGONSCAN_API_KEY=YOUR_POLYGONSCAN_API_KEY
```

---

## 2️⃣ Update `hardhat.config.js`

```javascript
networks: {
  polygon: {
    url: process.env.POLYGON_RPC_URL,
    accounts: [process.env.PRIVATE_KEY],
  },
},
etherscan: {
  apiKey: {
    polygonAmoy: process.env.POLYGONSCAN_API_KEY,
  },
},
```

---

## 3️⃣ Deploy to Polygon

```bash
npx hardhat run scripts/deploy.js --network polygon
```

---

## 4️⃣ Verify on PolygonScan

```bash
npx hardhat verify --network polygon DEPLOYED_CONTRACT_ADDRESS
```

View contract at:

```
https://amoy.polygonscan.com/address/YOUR_CONTRACT_ADDRESS
```

---

# 🔄 Update Frontend Contract Address

After deployment:

1. Copy deployed contract address  
2. Open your frontend config file  
3. Replace old contract address:

```javascript
export const contractAddress = "0xYourDeployedAddress";
```

4. Restart frontend:

```bash
npm run dev
```

---

# 💰 Getting Test Tokens

### Sepolia ETH Faucet:
https://sepoliafaucet.com/

### Polygon Amoy Faucet:
https://faucet.polygon.technology/

---

# ✅ Deployment Complete

Your Voting DApp is now live on:

- Ethereum Sepolia Testnet
- OR Polygon Testnet

You can now connect MetaMask and interact with the deployed smart contract.

---
