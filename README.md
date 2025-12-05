# Masterarbeit

## Overview

This framework provides a role-based access control system that allows users to manage who can access specific content. The system combines smart contracts, attestations, and encryption to create a flexible and secure content management solution.

## Key Features

### Role Management
Users can create their own access control sessions using smart contracts and assign role-based tags to different accounts. The system uses EAS (Ethereum Attestation Service) to create verifiable role attestations.

### Content Encryption
Through Lit Protocol integration, content owners can encrypt their data and configure precise access rules. Only users with the appropriate roles can decrypt and access the protected content.

### Decentralized Storage
Content is stored on IPFS, making it publicly available but only accessible to authorized users who can successfully decrypt it.

## Architecture

The project consists of three main components:

- **Smart Contracts**: Handle role assignments and access control logic
- **Backend**: Manages Lit Protocol integration and encryption operations
- **Frontend**: Provides the user interface built with SvelteKit

## Getting Started

### Prerequisites

Make sure you have the following installed:
- Node.js and npm
- A wallet for blockchain interactions

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
Note that you have to npm install in both the root directory and Frontend/ directory
   
3. Copy the example environment file and configure your settings:
   ```bash
   cp env.example .env
   ```

### Development

Run the development server in the Frontend/ directory :
```bash
npm run dev
```


### Deployment

Deploy contracts using Hardhat:
```bash
npx hardhat run scripts/deploy.ts --network <network-name>
```

## Project Structure

- `contracts/`: Solidity smart contracts for the access control system
- `Backend/`: Server-side logic including Lit Protocol integration
- `Frontend/`: SvelteKit application with user interface
- `scripts/`: Deployment and utility scripts
- `test/`: Contract tests 
