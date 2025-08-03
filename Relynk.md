# 🔗 Relynk - Web3 Creator Economy Platform

**Tagline:** _"Monetize anything. Own everything. On-Chain"_

A comprehensive Web3-native monetization platform that empowers creators, freelancers, and digital entrepreneurs to create payment links, sell digital products, and unlock content access — all without relying on Web2 platforms or centralized gatekeepers.

## 🎯 Overview

Relynk brings the simplicity of traditional payment link services like Gumroad or Mayar.id, but powered by **crypto, smart contracts, and self-custody**. It combines the ease of use of Web2 with the sovereignty and transparency of Web3.

## 🏗️ Project Structure

This repository contains the complete Relynk ecosystem:

```
relynk/
├── relynk-frontend/                 # Frontend application (Next.js)
└── relynk-contract/         # Smart contracts (Solidity)
```

### 📱 Frontend Application (`relynk-frontend/`)

The user-facing web application built with modern Web3 technologies:

- **Framework**: Next.js 15 with React 19 and TypeScript
- **Styling**: Tailwind CSS 4 with shadcn/ui components
- **Web3 Integration**: Wagmi, Viem, SIWE authentication
- **State Management**: TanStack Query
- **Authentication**: NextAuth.js with SIWE (Sign-In with Ethereum)

[🔗 Frontend Repository](https://github.com/Nekoo-Labs/relynk-frontend)

### ⚡ Smart Contracts (`relynk-contract/`)

Ethereum-compatible smart contracts powering the platform:

- **Framework**: Foundry (Solc 0.8.24)
- **Architecture**: Modular contract system
- **Network**: Deployed on Lisk Sepolia & Mainnet

[🔗 Contract Repository](https://github.com/Nekoo-Labs/relynk-contracts)

## ✨ Core Features

### 🔗 Onchain Payment Links
- Generate smart contract-backed payment links
- Support for ETH and ERC20 tokens (USDC, USDT, IDRX)
- Fixed price, dynamic price, or donation-based options
- Real-time payment notifications

### 📁 Digital Product Sales
- Upload files to IPFS for decentralized storage
- Automatic delivery after payment confirmation
- Support for eBooks, templates, design packs, courses
- Token-gated access control

### 👤 Creator Profiles
- Custom username registration (e.g., `relynk.xyz/username`)
- Personalized profile pages with social links
- Revenue analytics and earnings dashboard
- Profile metadata stored on IPFS

### 🎟️ Premium Content Access
- Subscription-based content unlocking
- One-time payment for lifetime access
- SBT/NFT-based proof of purchase
- Encrypted content delivery

### 💰 Creator Economics
- Low platform fees (2.5% default)
- Instant crypto payouts
- Multi-token support
- Revenue sharing capabilities

## 🚀 Deployed Contracts (Lisk Network)

### Lisk Sepolia (Testnet) - Chain ID: 4202

| Contract | Address | Description |
|----------|---------|-------------|
| **ProfileRegistry** | `0x00ceb34307a18d576e23c3719019bf3053f6c43b` | User profiles and username management |
| **RelynkProcessor** | `0x3b783177f8bb5ff07fc790e3a81b482fe55899bc` | Payment processing and content access |
| **MockUSDC** | `0x498f995ce39afcb27328ede058c3b09e4925d4a0` | Test USDC token (6 decimals) |
| **MockUSDT** | `0x0aa3e346f5d6eeef9b0574fe4831f62f4252d4f8` | Test USDT token (6 decimals) |
| **MockIDRX** | `0x7e00c1cebe298086b9fd9bd2897a0cefd14bc1d7` | Test Indonesian Rupiah token (18 decimals) |

### Network Details

- **Lisk Sepolia RPC**: `https://rpc.sepolia-api.lisk.com`
- **Lisk Mainnet RPC**: `https://rpc.api.lisk.com`
- **Block Explorer**: [Lisk Sepolia Explorer](https://sepolia-blockscout.lisk.com)
- **Faucet**: Available for testnet tokens

## 🛠️ Quick Start

### Prerequisites

- Node.js 18+ and npm/yarn
- Git
- Foundry (for contract development)

### 1. Clone the Repository

```bash
git clone https://github.com/Nekoo-Labs/relynk-frontend.git
cd relynk
```

### 2. Setup Frontend

```bash
cd paylynk
npm install
cp .env.example .env.local
# Configure environment variables
npm run dev
```

### 3. Setup Smart Contracts

```bash
cd relynk-contract
forge install
forge build
forge test
```

### 4. Deploy to Lisk (Optional)

```bash
# Deploy to Lisk Sepolia
forge script script/DeployRelynk.s.sol \
  --rpc-url https://rpc.sepolia-api.lisk.com \
  --private-key $PRIVATE_KEY \
  --broadcast
```

## 📖 Documentation

- [📱 Frontend Integration Guide](./paylynk/docs/integration-guide.md)
- [⚡ Smart Contract Documentation](./relynk-contract/docs/SMART_CONTRACT_DOCUMENTATION.md)
- [🚀 Deployment Guide](./relynk-contract/docs/DEPLOYMENT_GUIDE.md)
- [🔍 API Reference](./relynk-contract/docs/API_REFERENCE.md)
- [🧪 Testing Guide](./relynk-contract/docs/BLOCKCHAIN_EXPLORER_TESTING_GUIDE.md)

## 🔗 Links

- **Live Application**: [https://paylynk.vercel.app](https://paylynk.vercel.app)
- **Frontend Repository**: [GitHub - Relynk Frontend](https://github.com/Nekoo-Labs/relynk-frontend)
- **Contract Repository**: [GitHub - Relynk Contracts](https://github.com/Nekoo-Labs/relynk-contracts)
- **Documentation**: [Relynk Docs](./docs/)

## 🤝 Contributing

We welcome contributions! Please read our contributing guidelines in each respective folder:

- [Frontend Contributing](./paylynk/CONTRIBUTING.md)
- [Contract Contributing](./relynk-contract/CONTRIBUTING.md)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## 🏆 Built on LISK

Relynk was built with ❤️ for the Web3 creator economy. We believe in:

- **Creator Sovereignty**: Own your audience and revenue
- **Transparency**: All transactions on-chain and verifiable
- **Innovation**: Bridging Web2 UX with Web3 infrastructure
- **Community**: Building tools that empower creators globally

---

**Built by**: [Nekoo Labs](https://github.com/Nekoo-Labs)  
**Network**: Lisk Ecosystem  
**Current Version**: v1.0.0
