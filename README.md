# Create a Token

This Solidity program is a simple "Create a Token" program that demonstrates the basic syntax and functionality of the various token functions in this Solidity programming language. The purpose of this program is to burn and the mint the values of the token.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions mint and burn that increase the token by the value and burn the token by the value respectively". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

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

contract MyToken {
    // public variables here
    string public Token_Name = "Mansidak";
    string public Token_Abbev = "Sidak";
    uint public Total_Supply = 0; //uint because total supply can never be Negative
    // mapping variable here
 mapping(address => uint) public balances;
    // mint function
function mint(address _address, uint _value ) public {
 Total_Supply += _value;
 balances[_address] += _value;
 }
    // burn function

function burn(address _address, uint _value ) public {
 if(balances[_address]>= _value){
 Total_Supply -= _value;
 balances[_address] -= _value;
}
}
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile Token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function or burn function . Click on the "Token" contract in the left-hand sidebar, and then click on the variables,mint as well as burn function  function. Finally, click on the "transact" button to execute the function and retrieve the "Total Supply".

## Authors

Mansidak Singh  
[@mansidaksingh24@gmail.com)]

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
