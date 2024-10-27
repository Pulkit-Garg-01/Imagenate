# Imagenate - Decentralized AI Image Generation Platform

## Overview
Imagenate is a groundbreaking decentralized AI image generation platform built on the Galadriel network. This guide will walk you through setting up and deploying your first AI-powered image generation application.

## Table of Contents
- [System Requirements](#system-requirements)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Contract Deployment](#contract-deployment)
- [Using the Platform](#using-the-platform)
- [Technical Stack](#technical-stack)

## System Requirements
Before beginning, ensure you have:
- Node.js and npm installed on your development machine
- A Galadriel-compatible wallet with testnet tokens
- Basic familiarity with TypeScript and smart contracts

## Getting Started

### Account Setup
1. Create a new EVM wallet specifically for Imagenate development
2. Visit the [Galadriel Faucet Portal](https://docs.galadriel.com/faucet) to obtain test tokens
3. Save your wallet credentials securely

### Development Setup
```bash
# Initialize project
git clone https://github.com/yourusername/imagenate.git
cd imagenate

# Configure environment
cp config.example.env .env

# Required environment variables:
GALADRIEL_PRIVATE_KEY=your_private_key_here
GALADRIEL_ORACLE=0x4168668812C94a3167FCd41D12014c5498D74d7e
```

## Contract Deployment

1. Install project dependencies:
```bash
npm install
```

2. Deploy the Imagenate smart contract:
```bash
npm run deploy:imagenate
```

3. Store your contract address:
```bash
export IMAGENATE_CONTRACT=<deployed_contract_address>
```

## Using the Platform

### Generating Images
Execute the following to interact with your deployed contract:
```bash
npm run generate-image
```

The interactive CLI will prompt you for:
- Image description/prompt
- Generation parameters
- Output preferences

### Technical Stack
- Frontend: TypeScript/React
- Smart Contracts: Solidity
- AI Integration: Galadriel Oracle
- Development Tools: Hardhat, Ethers.js

### Integration Example
```typescript
const imagenate = await Imagenate.connect(signer);
const imageResult = await imagenate.generateImage({
  prompt: "your creative prompt here",
  parameters: {
    size: "1024x1024",
    style: "photorealistic"
  }
});
```

---

Built with 💫 by the Imagenate Team