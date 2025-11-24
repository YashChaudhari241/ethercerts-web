# EtherCerts-Web

A decentralized course certification platform that leverages blockchain technology to issue, manage, and verify educational certificates. Built with Next.js and Ethereum smart contracts.

## 🌟 Features

- **Web3 Authentication**: Sign in securely using MetaMask or Coinbase Wallet
- **Issue Certificates**: Authorized issuers can create blockchain-verified certificates
- **Certificate Verification**: Verify certificate authenticity on-chain
- **Encrypted Data**: Certificate details are encrypted and stored on the blockchain
- **Role-Based Access**: Owner, Authority, and Issuer roles with different permissions
- **Shareable Links**: Generate secure, shareable certificate links with decryption keys

## 🛠️ Tech Stack

- **Frontend**: Next.js, React
- **Styling**: Tailwind CSS
- **Web3**: Wagmi, ethers.js
- **Database**: Prisma ORM
- **Authentication**: Wallet-based signature authentication
- **Blockchain**: Ethereum (Hardhat local network / Goerli testnet)

## 📋 Prerequisites

- Node.js (v14 or higher)
- MetaMask or Coinbase Wallet browser extension
- A running instance of the smart contract (see [ethercerts-hardhat](../ethercerts-hardhat))

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/YashChaudhari241/course-certification.git
   cd course-certification
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure the database**
   ```bash
   npx prisma generate
   npx prisma db push
   ```

4. **Set up environment variables**
   Create a `.env` file in the root directory with necessary configurations.

5. **Update contract address**
   Ensure `hardhat.json` contains the deployed contract address from the Hardhat repository.

6. **Run the development server**
   ```bash
   npm run dev
   ```

7. **Open your browser**
   Navigate to `http://localhost:3000`

## 📱 Usage

### For Students
1. Connect your wallet (MetaMask/Coinbase)
2. Sign the authentication message
3. View all certificates issued to your wallet address
4. Share certificate links with decryption keys

### For Issuers
1. Connect your authorized issuer wallet
2. Navigate to the issuer page
3. Select a student and enter course details
4. Issue certificate - creates an encrypted on-chain record

### For Authorities
1. Manage authorized issuers
2. Add or remove issuer permissions
3. View authority status on the blockchain

## 🔗 Integration with Smart Contract

This frontend integrates with the Certify smart contract. Make sure to:
- Deploy the contract from [ethercerts-hardhat](../ethercerts-hardhat)
- Update `hardhat.json` with the deployed contract address
- Ensure the contract ABI is accessible in the artifacts folder

## 🔐 Security Features

- Wallet signature-based authentication
- Encrypted certificate data on-chain
- Role-based access control
- Nonce-based replay attack prevention
