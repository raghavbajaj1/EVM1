# FINAL PROJECT

This Solidity program is a Final Project program that demonstrates the basic syntax and functionality of the Solidity programming language.
## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The purpose of this program is to create a token(Token Name, Token Abbrv., Total Supply) . The contract has two functions , first one increases the total supply by that number and increases the balance of the address by that amount and second one deduct the value from the total supply and from the balance of the address. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a.sol extension (e.g., project.sol). Copy and paste the following code into the file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.7;

contract project {

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

    // public variables here
    string public name = "OHIYAAR";
    string public abbreviation = "HAAR";
    uint public supply ;

    // mapping variable here
    mapping(address => uint) map;
    
    // mint function
    function mint(address add,uint val) public {
        supply = supply + val;
        map[add] = map[add] + val;
    }

    // burn function
    function burn(address add,uint val) public {
        if(map[add] >= val){
            supply = supply - val;
            map[add] = map[add] - val;
        }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.7" (or another compatible version), and then click on the "Compile project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling both the functions. 

## Author

Raghav
STUDENT
CHANDIGARH UNIVERSITY
