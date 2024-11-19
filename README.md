# Fake Product Identification Using Blockchain
## Introduction
The Fake Product Identification system uses blockchain technology to verify the authenticity of products. This manual guides you through setting up, deploying, and using the project in a Hardhat environment.
## Prerequisites
Before using the project, ensure you have the following installed on your system:

Node.js: Version 18 or higher is recommended.

NPM: Comes bundled with Node.js.

Hardhat: Installed as a development dependency in the project.

MetaMask: Browser extension for managing blockchain accounts.

React.js: For frontend
## Project Setup
1. Clone the repository
   git clone 'git repository url'
   cd foldername
2. Install Dependencies
   npm install
3. Cofigure hardhat
   Hardhat is the development environment for compiling, deploying and testing the smart contracts.
   Hardhat Configuration File
   The hardhat.config.js file includes:
   Network settings (e.g., localhost, testnets like Rinkeby, mainnet)
   Compiler version (Solidity 0.8.0 or higher)
4. Compile the samrt contract
   npx hardhat compile
5. Start a local blockchain in another terminal
   npx hardhat node
7. Deploy the deploy.js file
   npx hardhat run scripts/deploy.js --network localhost

## Using the System
### Set up the Frontend
1. Navigate to the frontend directory
   cd frontend
2. Start the React App
   npm start
### Connect Metamask
Once the application is opened, click on the connect to metamask
Make sure 'Hardhat' is selected in the metamask, import some accounts and connect the wallet to the react app.
## Interact with the Application
### Add Product
Open the application in your browser.
Enter product details
Click Add Product. Confirm the transaction in MetaMask.
### Add a Distributor
Give the required details and confirm the transaction in the metamask.
### Track your products
You can track the added products.
### Authenticating Product
Verify the product by scanning the generated QR code.
## Key Components

### Smart Contract (FakeProduct.sol)

Defines the structure for adding and retrieving product details on the blockchain.

### Deployment Script (deploy.js)

Automates the deployment of the smart contract.

### Frontend (React)

Provides a user interface for interacting with the blockchain.

### Hardhat Environment

Manages smart contract compilation, testing, and deployment.

## Troubleshooting

### Common Errors

1. Artifact Not Found

Ensure you’ve compiled the contracts:

npx hardhat compile

2. Transaction Fails

Verify that MetaMask is connected to the correct network.

Ensure sufficient funds for gas.

3. Missing start Script

Ensure your frontend/package.json includes:

"scripts": {
  "start": "react-scripts start"
}

### Node.js Version Warning

If you see a warning about unsupported Node.js versions, switch to a stable version

## Future Enhancements

Improve the QR code scanning method for product verification.

Add multi-signature verification.

Enable product batch processing.
