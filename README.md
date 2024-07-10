# ERC20 Token

This is a simple program that demonstrates how to create own ERC20 token and deploy it using Remix.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a constructor and two functions mint and burn.
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Project3.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Token is ERC20 {
    constructor() ERC20("Token", "TK") {
        _mint(msg.sender, 5000 * 1 ** decimals());
    }

    function mint(address to, uint256 amount) public {
        _mint(to, amount);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.20", and then click on the "Compile Project3.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar.

Once the contract is deployed, you can interact with it by calling the functions mint and burn. Pass address and value to mint function and click on transact you can see total supply will increase by that value.
Pass value to burn function and click on transact it will reduce total supply by that value.

## Authors
Rajnish Kumar
