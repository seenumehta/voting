# Election Voting Smart Contract

## Overview
The **Election Voting** smart contract is a blockchain-based voting system built with Solidity. It provides a transparent and secure way to conduct elections, ensuring that each voter can only vote once and that results are immutable.

## Features
- **Candidate Registration**: The election commission can add candidates.
- **Voter Authorization**: Only authorized voters can participate.
- **Secure Voting**: Each voter can vote only once.
- **Tamper-Proof Results**: Vote counts are immutable and publicly verifiable.
- **Decentralized & Transparent**: No central authority can alter votes once cast.

## Smart Contract Functions
### 1. `addCandidate(string memory _name)`
Allows the election commission to register candidates.
```solidity
function addCandidate(string memory _name) public onlyCommission
```

### 2. `authorizeVoter(address _voter)`
Grants voting rights to a specified address.
```solidity
function authorizeVoter(address _voter) public onlyCommission
```

### 3. `vote(uint _candidateId)`
Enables a registered voter to cast their vote.
```solidity
function vote(uint _candidateId) public
```
- Ensures the voter is authorized and has not voted before.

### 4. `getResults(uint _candidateId)`
Retrieves the current vote count for a candidate.
```solidity
function getResults(uint _candidateId) public view returns (string memory, uint)
```

## Deployment
1. Deploy the contract on an Ethereum-compatible blockchain.
2. Use Web3.js, Ethers.js, or a frontend to interact with the contract.


## Author
Developed by [Anoop]

