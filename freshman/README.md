## Freshman
https://www.learnweb3.io/tracks/freshman
https://github.com/fabricegeib/learnweb3/tree/master/freshman

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

### ⚒️ Level 9 - ✅ (100%)
Skill test can be found at the end of the level

Setup Hardhat :
```shell
mkdir NFT-Tutorial
cd  NFT-Tutorial
npm init --yes
npm install --save-dev hardhat

npx hardhat
```

Create a basic sample project

git tag -a v1.0.1 -m "First release for v1.0.1"

npm install --save-dev "hardhat@^2.9.1" "@nomiclabs/hardhat-waffle@^2.0.0" "ethereum-waffle@^3.0.0" "chai@^4.2.0" "@nomiclabs/hardhat-ethers@^2.0.0" "ethers@^5.0.0"

npm install --save-dev @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers

### Write NFT Contract
npm install @openzeppelin/contracts

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

// Import the openzepplin contracts
import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

// GameItem is  ERC721 signifies that the contract we are creating imports ERC721 and follows ERC721 contract from openzeppelin
contract GameItem is ERC721 {

    constructor() ERC721("GameItem", "ITM") {
        // mint an NFT to yourself
        _mint(msg.sender, 1);
    }
}
```

`npx hardhat compile`

### Deploy
In folder `script` create a file `deploys.js `
```js
// Import ethers from Hardhat package
const { ethers } = require("hardhat");

async function main() {
  /*
A ContractFactory in ethers.js is an abstraction used to deploy new smart contracts,
so nftContract here is a factory for instances of our GameItem contract.
*/
  const nftContract = await ethers.getContractFactory("GameItem");

  // here we deploy the contract
  const deployedNFTContract = await nftContract.deploy();

  // print the address of the deployed contract
  console.log("NFT Contract Address:", deployedNFTContract.address);
}

// Call the main function and catch if there is any error
main()
  .then(() => process.exit(0))
  .catch((error) => {
    console.error(error);
    process.exit(1);
    });
```
NFT Contract Address: 0x0EB540EDd3e58794Ca136218bA5c10B9c66b0164

https://rinkeby.etherscan.io/address/0x0EB540EDd3e58794Ca136218bA5c10B9c66b0164
https://rinkeby.etherscan.io/token/0x0EB540EDd3e58794Ca136218bA5c10B9c66b0164