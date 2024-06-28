# __FootballFanToken (FFT) Contract__

FootballFanToken is an ERC20 token contract implemented in Solidity. It utilizes OpenZeppelin's ERC20 and Ownable contracts to provide standard token functionality and ownership control.
# Description

FootballFanToken (FFT) is an ERC20 token built on the Ethereum blockchain, designed specifically for football fans. This token allows fans to engage and interact within the football community.
With functionalities like minting and burning tokens, FFT provides a flexible and community-driven experience.

Features
Minting: Only the owner of the contract can mint new tokens.
Burning: Token holders can burn their tokens, reducing the total supply.
Balance Check: Users can check the balance of any address.




## Getting Started
### Installing
To download the code, you can visit the following file path:-[https://github.com/Paaapi/Etherreum/blob/main/assessment3.sol]

## Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at (https://remix.ethereum.org/.)

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Meta.sol). Copy and paste the following code into the file: contract MyToken
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract FootballFanToken is ERC20, Ownable {
    constructor() ERC20("FootballFanToken", "FFT") Ownable(msg.sender) {
        // Mint initial supply to the contract deployer (owner)
        _mint(msg.sender, 1000000 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }

    // Function to retrieve the balance of an address
    function balance(address account) public view returns (uint256) {
        return balanceOf(account);
    }
}


   

 
   
```
## Authors
Paravdeep (paravdeepwalia@gmail.com)

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
