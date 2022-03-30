# Simple Ethereum Dapp 

This project demonstrates the use of Hardhat + React + Ethers.js by developing a simple ERC20 contract. Follow the steps here: [The Complete Guide to Full Stack Ethereum Development](https://dev.to/dabit3/the-complete-guide-to-full-stack-ethereum-development-3j13)

## Notes:
- testnet ETH for the Rinkeby network were taken from [chainlink faucet](https://faucets.chain.link/rinkeby)

## Setup project:
```
npx create-react-app react-dapp
(change into react-dapp directory) 
npm install ethers hardhat @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers
npx hardhat
```
- Make necessary changes in hardhat.config.js
```
module.exports = {
  solidity: "0.8.4",
  paths: {
    artifacts: './src/artifacts',
  },
  networks: {
    hardhat: {
      chainId: 1337
    }
  }
};
```
- Configure hardhat.config.js to use env file:
```
require("dotenv").config({ path: __dirname + "/.env" });
const { API_URL, PRIVATE_KEY } = process.env;
```

## Run project:
```
(start hardhat network) npx hardhat node
(compile) npx hardhat compile
(run script) npx hardhat run scripts/deploy.js --network localhost
(start REACT server) npm start
```
