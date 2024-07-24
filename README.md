# Swisstronik Tesnet Techinal Task 2

## Steps

### 1. Clone Repository

```bash
git clone https://github.com/tianpratama1109/swisstronik-mint-token-erc20.git
```

```
cd swisstronik-erc20-mint-token
```

### 2. Install Dependency

```bash
npm install
```

### 3. Set Up .env File

Create a .env file in the root of the project:

```bash
PRIVATE_KEY="your private key"
```

### 4. Create Smart Contract

- Open the contract folder
- Create a Token.sol file
- Copy and paste the following code, modifying the token name and symbol as needed:
- Feel free to modify token name and token symbol

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract TestToken is ERC20 {
    constructor()ERC20("IzzyToken","IZZY"){}

    function mint1000tokens() public {
        _mint(msg.sender,1000*10**18);
    }

    function burn1000tokens() public{
        _burn(msg.sender,1000*10**18);
    }

}
```

### 5. Compile Smart Contract

```bash
npm run compile
```

### 6. Deploy Smart Contract

```bash
npm run deploy
```

### 7. Mint Token

```bash
npm run mint
```

### 8. Check Supply

```bash
npm run check-supply
```

### 9. Check Balance

```bash
npm run balance-of
```

### 10. Transfer Tokens

```bash
npm run transfer
```

### 11. Finsihed

- Open the deployed-address.ts file (located in the utils folder)
- Copy the address and paste it into the testnet dashboard
- Push this project to your GitHub and paste your repository link into the testnet dashboard
