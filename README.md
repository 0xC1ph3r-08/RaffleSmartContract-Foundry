# 🎲 Decentralized Raffle Smart Contract
This repository contains a Solidity smart contract for a fully decentralized, provably fair raffle system. Built with Foundry, this project leverages Chainlink VRF (Verifiable Random Function) for secure and verifiable randomness, and Chainlink Automation (Keepers) to automatically trigger the winner selection process.

## Quick Start
```terminal
git clone https://github.com/Cyfrin/foundry-smart-contract-lottery-cu
cd foundry-smart-contract-lottery-cu
forge build
```
### Usage 
```terminal
make anvil
```
### Library
If you're having a hard time installing the chainlink library, you can optionally run this command.
```terminal
forge install smartcontractkit/chainlink-brownie-contracts@0.6.1
```
### Deploy (Locally)
```terminal
make deploy
```

### Deploy to Sepolia 
```terminal 
make deploy-sepolia
```

## ✨ Features

**Decentralized:** Runs entirely on the blockchain (Sepolia Testnet, or local Anvil).
Provably Fair Randomness: Utilizes Chainlink VRF to ensure that the winner selection is genuinely random and auditable by anyone.
**Automated Winner Selection:** Integrated with Chainlink Automation (Keepers) to automatically check if raffle conditions are met and trigger the winner drawing process at set intervals, without manual intervention.
Open & Transparent: All participants and winning logic are visible on the blockchain.


## 💡 How it Works (Simple Flow)
**Enter Raffle:** Players can send the required entrance fee to the contract to join the current raffle round.
**Automated Check:** Once a set time interval passes and there are participants, Chainlink Automation detects that the raffle is ready to pick a winner.
**Randomness Request:** Chainlink Automation triggers the contract to request a provably random number from Chainlink VRF.
**Winner Selection:** Chainlink VRF delivers the random number back to the contract, which then uses it to fairly select a winner from the pool of participants. The prize (collected entrance fees) is sent to the winner.
Reset: The raffle automatically resets for the next round, ready for new participants.


**🛠️ Technologies Used**
**Solidity**: Smart contract language.
**Foundry**: Fast, modern, and modular toolkit for Ethereum application development.
**Chainlink** VRF: For secure and verifiable on-chain randomness.
**Chainlink** Automation (Keepers): For decentralized and automated smart contract execution.


**NOTE :** This is a brief about the contract and i am gonna provide the link of the `blog` where i will explain this contract / project in depth .

