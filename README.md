# learnweb3

## Freshman
https://www.learnweb3.io/tracks/freshman

### 🔗 Level 0 - Basic Programming ✅ (100%)

### 🔗 Level 1 - What is Blockchain? ✅ (100%)

### 🔗 Level 2 - What is Web3 ✅ (100%)

### 🔗 Level 3 - What is ETH ✅ (100%)

### 🔗 Level 4 - Crypto Wallets ✅ (100%)

### 🔗 Level 5 - Remix IDE ✅ (100%)

### 🔗 Level 6 - Solidity ✅ (100%)

### ⚒️ Level 7 - dApp ✅ (100%)
Skill test can be found at the end of the level

### Install a http server (use any you like)
```shell
npm install --global http-server

npx http-server
npx http-server --cors

# or

npm install -g lite-server #install lite-server globally
```

### Create and Serve a Simple Webpage

Create a file `index.html`

```html
<html>
    <body>
        <h1>This is my dApp!</h1>
        <p>Here we can set or get the mood:</p>
        <label for="mood">Input Mood:</label> <br />
        <input type="text" id="mood" />
        <div>
            <button onclick="getMood()">get Mood</button>
        </div>
        <div>
            <button onclick="setMood()">set Mood</button>
        </div>
    </body>
</html>
```

### Contract on Rinkeby
0xCe1b98929515223B576fE6DA62102276C0fb8604

https://rinkeby.etherscan.io/address/0xce1b98929515223b576fe6da62102276c0fb8604

### Start the front
```
npx http-server
```

### ⚒️ Level 8 - Cryptocurrency ✅ (100%)
Skill test can be found at the end of the level

### Contract
`LW3Token.sol`

```sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol";

contract LW3Token is ERC20 {
    constructor(string memory _name, string memory _symbol) ERC20(_name, _symbol) {
        _mint(msg.sender, 10 * 10 ** 18);
    }
}
```

LearbWeb3 Token (10 LW3)
https://rinkeby.etherscan.io/address/0x721cc4a419950d234a5fc1ecdebbc9f1ba155ccd
https://rinkeby.etherscan.io/token/0x721cc4a419950d234a5fc1ecdebbc9f1ba155ccd
Transfer to 0x000000000000000000000000000000000000dead

LearnWeb3 Token (1000 LW3)
https://rinkeby.etherscan.io/address/0xc4bd4275ba2a12e2aad0c7ff4fb57ab8c3b07f26
https://rinkeby.etherscan.io/token/0xc4bd4275ba2a12e2aad0c7ff4fb57ab8c3b07f26

### ⚒️ Level 9 - NFT ❌ (0%)
Skill test can be found at the end of the level

Setup Hardhat :
```shell
mkdir NFT-Tutorial
cd  NFT-Tutorial
npm init --yes
npm install --save-dev hardhat
```

## Sophomore
https://www.learnweb3.io/tracks/sophomore

## Junior
https://www.learnweb3.io/tracks/junior

## Senior
https://www.learnweb3.io/tracks/senior