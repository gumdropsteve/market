### Installing

First, you will need to install the dependencies with: npm install.

Run the following command in your terminal after cloning the main repo:

$ npm install


Then, you will need to install Truffle globally by running the following command int your terminal:

$ npm install -g truffle


### Running the Tests

First, you will have to compile the smart contracts by running the following command in your terminal:

$ truffle compile


Then you will have to install and run Ganache to run your blockchain locally:

https://www.trufflesuite.com/ganache

Then, the tests that validate your solution can be executed by runing the following
command:

$ truffle test


### Deployment on Local Blockchain

Deploy the contracts on your Ganache local blockchain by running the following command:

$ truffle migrate


### Opening the User Interface

First of all, it is required to install Metamask wallet as a browser extension: https://metamask.io/

Then you should configure Metamask to connect to your local blockchain run by Ganache. This requires the following:
- Open Metamask
- Open the Network Configuration panel
- Open Custom RPC
- Configure your private network by adding http://localhost:7545 on the URL and 1337 as a chain ID.
- Import the first Ganache Account to Metamask by copying the Account Private Key from Ganache and pasting it on Metamask

Finally you just need to run the following command in your terminal to open the User Interface:

$ npm start


### Deployment on Public Network

In order to deploy your smart contract, you must create your .env file and specify:

- PRIVATE_KEYS --> Private Key of the account you are using to deploy (typically the first one in the list of Ganache)
- INFURA_API_KEY --> API key provided by Infura: https://infura.io/

Then, you will need to run the following command (let's use the testnet Ropsten in this example, remember to request some Ether for your account using a faucet):

$ truffle migrate --network ropsten


Finally you can run the following command to generate the build artifacts of your User Interface and then deploy to your favourite host:

npm run build



### Technology stack

- Solidity
- React.js
- Truffle
- Web3.js
- Ganache
- Node.js
- Metamask
- IPFS

## The Project

This project consists in an open platform where each user can mint his own NFT and expose it on a marketplace by making an offer or buying NFT from others. It includes:

- A smart contract which represents a collection of NFTs by following the ERC-721 standard
- A smart contract which represents the NFT Marketplace and contains all the logic to make offers, fill offers...
- Tests built with JavaScripts to ensure smart contracts are accomplishing the expected functionalities
- A React.js front-end application as a user interface
