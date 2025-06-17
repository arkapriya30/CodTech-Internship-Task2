# Task 2 – Custom ERC-20 Token (PriyaToken)

## Description
This project is part of the CodTech Blockchain Internship Task 2. It involves creating and deploying a custom ERC-20 token using Solidity and Hardhat.

## Tools Used
- Solidity
- Hardhat
- OpenZeppelin Contracts
- Replit (Node.js environment)

## Token Details
- *Token Name*: PriyaToken
- *Symbol*: SGT
- *Decimals*: 18 (default)
- *Initial Supply*: 1000 SGT (minted to deployer's address)

## Contract Code
The token is based on OpenZeppelin’s secure ERC-20 standard:

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("PriyaToken", "SGT") {
        _mint(msg.sender, initialSupply * 10 ** decimals());
    }
}
```


## Deployment Steps

1. Compile the contract:
   ``` bash
   npx hardhat compile
   ```


2. Run the deployment script (Hardhat in-memory testnet):
  ``` bash
   npx hardhat run scripts/deploy.js
   ```


3. Deployment Output:
````

   🎉 PriyaToken deployed to:
   0x5FbDB2315678afecb367f032d93F642f64180aa3
   ````


> ✅ Note: Deployed using Hardhat's in-memory testnet on Replit

## Screenshot
![screenshot](screenshot.png)