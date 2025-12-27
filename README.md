# Zama-name-Service
Zama Name Service (ZNS) A decentralized, privacy-preserving name service built on FHEVM using Fully Homomorphic Encryption to keep name data encrypted on-chain.

# Zama Name Service (ZNS)

Zama Name Service (ZNS) is a decentralized and privacy-preserving name service built on **FHEVM** using **Fully Homomorphic Encryption (FHE)**.  
It enables users to register and manage human-readable names while keeping sensitive name metadata encrypted on-chain.

Unlike traditional name services, ZNS ensures that private data remains confidential even during computation, leveraging Zama’s FHE technology.

---

## 🚀 Features

- 🔐 **Encrypted Name Records**  
  Name metadata is stored and processed in encrypted form using FHE.

- 🧠 **FHEVM Powered**  
  Built on Zama’s Fully Homomorphic Encryption Virtual Machine.

- 🌐 **Decentralized Ownership**  
  Names are owned and controlled by user wallets.

- 🖥 **Simple Web Interface**  
  Frontend for registering and interacting with encrypted names.

---

## 🛠 Tech Stack

### Smart Contracts
- Solidity
- FHEVM (Zama)
- Hardhat

### Frontend
- Next.js
- Ethers.js
- MetaMask

---

## 📁 Repository Structure

📁 Repository Structure

zama-name-service/
├── pages/
│   └── index.tsx
├── components/
├── hooks/
├── lib/
├── public/
├── styles/
├── next.config.mjs
├── package.json
└── README.md

yaml
Copy code

---

## 🔑 How It Works

1. A user submits a name via the frontend.
2. Name metadata is encrypted using FHE-compatible types.
3. The encrypted data is stored on-chain via the smart contract.
4. Ownership and encrypted state are maintained without revealing sensitive information.

---

## 🌍 Demo

- **Frontend Demo**:   
- **Smart Contract**: Deployed on an FHEVM-compatible testnet

---

## 📌 Use Cases

- Private domain name systems
- Encrypted identity layers
- Confidential Web3 naming infrastructure
- Privacy-first decentralized applications

---

## 🔮 Future Improvements

- Name expiry and renewal
- Minting fee support
- Subdomains
- Resolver integration
- Multi-chain deployment

---

## 📄 License

MIT License
