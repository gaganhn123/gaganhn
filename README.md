# MyToken
This Solidity program is a simple contract that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description
This program is a contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions that allow you to mint and burn tokens.When a certain amount of tokens are passed with the address its either minted i.e. when the mint function is called tokens are added in the address and similarly when the burn function is called tokens are subtracted in the address. This program serves as a simple and straightforward introduction to Solidity programming.

## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "GAGAN";
    string public tokenAbbrv = "HN";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint (address tokenaddr,uint value) public {
        totalSupply += value;
        balances[tokenaddr] += value;
    }
    // burn function
    function burn (address tokenaddr,uint value) public {
        if (balances[tokenaddr] >= value){
            totalSupply -= value;
            balances[tokenaddr] -= value;
        }
    }

}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling its functions. Click on the "MyToken" contract in the left-hand sidebar, and then click on any of its functions to interact with it.

## Authors
GAGAN HN
@gaganhn2004@gmail.com

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
