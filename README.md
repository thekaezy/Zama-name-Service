# 🔐 Zama Name Service (ZNS)

> **Private Identity for the On-Chain World**  
> A decentralized, privacy-preserving name service built on FHEVM (Fully Homomorphic Encryption Virtual Machine) that keeps your identity data encrypted and confidential on the blockchain.

![Zama Name Service Banner]<img width="1896" height="805" alt="image" src="https://github.com/user-attachments/assets/2bf5cce2-9cc1-4ade-bb29-861210fac691" />

---

## 🌟 What is Zama Name Service?

Zama Name Service (ZNS) is a **privacy-first blockchain naming system** that allows users to register human-readable names while keeping sensitive information **encrypted on-chain**. Unlike traditional naming services (like ENS), ZNS leverages **Fully Homomorphic Encryption (FHE)** to ensure:

- ✅ **End-to-End Encryption** - Name data remains encrypted even during computation
- ✅ **Zero-Knowledge Privacy** - No one (not even miners) can see your data
- ✅ **Decentralized Ownership** - You control your identity
- ✅ **Blockchain Verification** - All transactions are verifiable on Sepolia testnet

---

🌐 **Try it now:** (https://zama-name-service.vercel.app/)

📜 **Smart Contract:** `0x9B25734e69D073897fA82CEF5f7A77Adb6450ea7` ([View on Etherscan](https://sepolia.etherscan.io/address/0x9B25734e69D073897fA82CEF5f7A77Adb6450ea7))

---

## 🎯 Key Features

### 🔒 Privacy-First Design
- **Encrypted Name Storage** - All name metadata stored using FHE encryption
- **Confidential Registration** - Register names without revealing sensitive data
- **Private Ownership** - Only you can access your encrypted information

### ⚡ User-Friendly Interface
- **Wallet Integration** - Seamless MetaMask connection
- **Name Search** - Check availability before registering
- **Real-Time Updates** - Instant confirmation on Sepolia network
- **Transaction History** - View all registrations on Etherscan

### 🛡️ Powered by FHEVM
- **Fully Homomorphic Encryption** - Compute on encrypted data
- **Zama Protocol** - Industry-leading FHE technology
- **Sepolia Testnet** - Deployed on Ethereum's test network

---

## 🏗️ Project Structure

```
zama-name-service/
│
├── 📁 contracts/              # Smart Contract Files
│   ├── FHENameService.sol    # Main FHEVM contract
│   └── FHECounter.sol        # Example FHE contract
│
├── 📁 deploy/                 # Deployment Scripts
│   ├── deploy.ts             # Example deployment
│   └── 001_deploy_name_service.ts  # Name service deployment
│
├── 📁 pages/                  # Next.js Pages
│   ├── _app.tsx              # App wrapper
│   └── index.tsx             # Main landing page
│
├── 📁 components/             # React Components
│   ├── Header.tsx            # Navigation header
│   ├── NameSearch.tsx        # Name availability checker
│   ├── RegisterForm.tsx      # Registration form
│   └── WalletConnect.tsx     # MetaMask integration
│
├── 📁 hooks/                  # Custom React Hooks
│   ├── useContract.ts        # Contract interaction hook
│   ├── useWallet.ts          # Wallet connection hook
│   └── useFHEVM.ts           # FHEVM-specific logic
│
├── 📁 contexts/               # React Context Providers
│   └── Web3Context.tsx       # Global web3 state
│
├── 📁 lib/                    # Utility Functions
│   ├── contract.ts           # Contract helpers
│   └── encryption.ts         # FHE encryption utils
│
├── 📁 types/                  # TypeScript Types
│   └── index.ts              # Type definitions
│
├── 📁 styles/                 # CSS/Styling
│   └── globals.css           # Global styles
│
├── 📁 public/                 # Static Assets
│   └── logo.png              # Project logo
│
├── 📁 test/                   # Test Files
│   └── FHENameService.test.ts
│
├── package.json               # Dependencies
├── tsconfig.json              # TypeScript config
├── hardhat.config.ts          # Hardhat config
├── next.config.mjs            # Next.js config
└── README.md                  # This file
```

---

## 🛠️ Tech Stack

### Smart Contracts
- **Solidity ^0.8.24** - Smart contract language
- **FHEVM** - Fully Homomorphic Encryption VM by Zama
- **Hardhat** - Ethereum development environment
- **Ethers.js** - Blockchain interaction library

### Frontend
- **Next.js 14** - React framework
- **TypeScript** - Type-safe JavaScript
- **TailwindCSS** - Utility-first CSS framework
- **Ethers.js v6** - Web3 library
- **MetaMask** - Wallet integration

### Deployment
- **Vercel** - Frontend hosting
- **Sepolia Testnet** - Smart contract deployment
- **IPFS** - Decentralized storage (future)

---

## 📋 Prerequisites

Before you begin, ensure you have:

- ✅ **Node.js v20.x** (use LTS version)
- ✅ **npm or pnpm** package manager
- ✅ **MetaMask** browser extension
- ✅ **Sepolia ETH** ([Get from faucet](https://sepoliafaucet.com/))
- ✅ **Infura API Key** ([Get here](https://infura.io/))

---

## 🚀 Quick Start

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/thekaezy/zama-name-service.git
cd zama-name-service
```

### 2️⃣ Install Dependencies

```bash
# Using npm
npm install

# Or using pnpm
pnpm install
```

### 3️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```env
# Hardhat Configuration
MNEMONIC="your twelve word seed phrase here"
INFURA_API_KEY="your_infura_api_key_here"

# Frontend Configuration
NEXT_PUBLIC_CONTRACT_ADDRESS="0x9B25734e69D073897fA82CEF5f7A77Adb6450ea7"
NEXT_PUBLIC_CHAIN_ID=11155111
```

### 4️⃣ Compile Smart Contracts

```bash
npx hardhat compile --network sepolia
```

### 5️⃣ Deploy to Sepolia (Optional)

```bash
npx hardhat deploy --network sepolia --tags FHENameService
```

**Save the deployed contract address!**

### 6️⃣ Run Frontend Locally

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📖 How It Works

### Registration Flow

```
1. User connects MetaMask wallet
   ↓
2. User enters desired name (e.g., "alice.zama")
   ↓
3. Frontend checks name availability
   ↓
4. User pays 0.001 ETH registration fee
   ↓
5. Name data is encrypted using FHE
   ↓
6. Transaction is sent to FHENameService contract
   ↓
7. Name is registered on-chain (encrypted)
   ↓
8. User receives confirmation + Etherscan link
```

### Contract Functions

```solidity
// Check if name is available
function isNameAvailable(string memory name) public view returns (bool)

// Register a new name
function registerName(string memory name) external payable returns (uint256)

// Get name owner (public)
function getNameOwner(string memory name) external view returns (address)

// Transfer name to another address
function transferName(string memory name, address newOwner) external
```

---

## 🔐 Privacy & Security

### How FHE Protects Your Data

**Traditional Blockchain:**
```
Input → [Public Processing] → Public Result
❌ Everyone can see your name data
```

**Zama Name Service (FHE):**
```
Input → [Encrypted Processing] → Private Result
✅ Data stays encrypted on-chain
✅ Only you can decrypt with your private key
```

### What's Encrypted?
- ✅ Name metadata
- ✅ Registration timestamps
- ✅ Custom descriptions
- ❌ Name ownership (intentionally public for verification)

---

## 🧪 Testing

### Run Smart Contract Tests

```bash
# Run all tests
npx hardhat test

# Run tests on Sepolia
npx hardhat test --network sepolia

# Check test coverage
npx hardhat coverage
```

### Example Test Output

```
  FHENameService
    ✓ Should allow name registration (2s)
    ✓ Should prevent duplicate names (1s)
    ✓ Should transfer name ownership (2s)
    ✓ Should maintain privacy for encrypted data (1s)

  4 passing (6s)
```

---

## 📊 Smart Contract Details

### Deployed Contract Info

| Network | Address | Explorer |
|---------|---------|----------|
| Sepolia Testnet | `0x9B25734e69D073897fA82CEF5f7A77Adb6450ea7` | [View on Etherscan](https://sepolia.etherscan.io/address/0x9B25734e69D073897fA82CEF5f7A77Adb6450ea7) |

### Contract Features

```solidity
// Contract: FHENameService.sol
pragma solidity ^0.8.24;

import { FHE, euint64 } from "@fhevm/solidity/lib/FHE.sol";
import { ZamaEthereumConfig } from "@fhevm/solidity/config/ZamaConfig.sol";

contract FHENameService is ZamaEthereumConfig {
    // Encrypted registration timestamps
    mapping(bytes32 => euint64) private registrationTime;
    
    // Public name ownership
    mapping(bytes32 => address) public nameOwners;
    
    // Registration fee: 0.001 ETH
    uint256 public registrationFee = 0.001 ether;
    
    // ... more contract logic
}
```

---

## 🎨 Screenshots

### Homepage
![Homepage](<img width="1903" height="552" alt="image" src="https://github.com/user-attachments/assets/d9396e31-8b0c-4c6d-a9b5-9c52b29449e1" />)

### Name Registration
![Register](<img width="1737" height="618" alt="Screenshot 2025-12-30 225400" src="https://github.com/user-attachments/assets/bc903905-a345-4c82-9c42-cca5937dc30c" />
)

### Transaction Confirmation
![Confirmation](<img width="1640" height="519" alt="image" src="https://github.com/user-attachments/assets/07eabf8b-2768-4262-90dd-52c804848852" />)

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

---

## 🐛 Known Issues

- [ ] Gas optimization needed for batch registrations
- [ ] Add name expiry and renewal functionality
- [ ] Implement subdomain support
- [ ] Add resolver integration for dApp compatibility

---

## 🗺️ Roadmap

### Phase 1 (Current) ✅
- [x] Basic name registration
- [x] FHE encryption integration
- [x] Sepolia testnet deployment
- [x] Frontend with wallet connection

### Phase 2 (Q1 2026)
- [ ] Name expiry and renewal system
- [ ] Subdomain support
- [ ] Batch registration discounts
- [ ] Enhanced privacy features

### Phase 3 (Q2 2026)
- [ ] Mainnet deployment
- [ ] Multi-chain support
- [ ] Resolver integration
- [ ] Mobile app

---

## 📚 Resources

### FHEVM & Zama
- 📖 [Zama FHEVM Documentation](https://docs.zama.ai/fhevm)
- 💻 [FHEVM GitHub](https://github.com/zama-ai/fhevm)
- 🎓 [FHE Tutorial](https://docs.zama.ai/protocol/solidity-guides)

### Tools Used
- 🔨 [Hardhat](https://hardhat.org/)
- ⚛️ [Next.js](https://nextjs.org/)
- 🦊 [MetaMask](https://metamask.io/)
- 🌐 [Ethers.js](https://docs.ethers.org/)

---

## 📄 License

This project is licensed under the **MIT License** - see the (LICENSE) file for details.

---

## 👥 Authors

**Your Name**
- GitHub:  (https://github.com/YOUR_USERNAME](https://github.com/thekaezy/Zama-name-Service))
- Twitter: (https://twitter.com/YOUR_TWITTER](https://x.com/KaezyXBT))
- Website: (https://your-website.com](https://zama-name-service.vercel.app/))

---

## 🙏 Acknowledgments

- **Zama Team** - For developing FHEVM and FHE technology
- **Ethereum Foundation** - For Sepolia testnet
- **Vercel** - For frontend hosting
- **OpenZeppelin** - For secure smart contract patterns

---

## 💬 Support

Need help? Have questions?

- 📧 Email: your.email@example.com
- 💬 Discord: [Join Zama Discord](https://discord.gg/zama)
- 🐦 Twitter: [@zama_fhe](https://twitter.com/zama_fhe)
- 📝 [Open an Issue](https://github.com/YOUR_USERNAME/zama-name-service/issues)

---

## ⚠️ Disclaimer

This project is currently deployed on **Sepolia testnet** for demonstration purposes. Use testnet ETH only. Do not send real funds.

The FHE encryption demonstrated here uses **hash-based privacy** for educational purposes. Production applications should use Zama's full FHEVM library with actual homomorphic encryption.

---

<div align="center">

**Built with ❤️ using FHEVM**

Made possible by [Zama](https://www.zama.ai/) 🔐

[⬆ Back to Top](#-zama-name-service-zns)

Made By @kaezyXbt with love
