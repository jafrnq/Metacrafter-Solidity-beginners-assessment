# MYTOKEN PROJECT README
This Solidity program is a simple token program that demonstrates the concept of minting and burning tokens using the solidity
programming language. This is a good starting point for those who are new to Solidity.

## Description

This README provides an overview of the small project "MyToken," which is a simple Solidity smart contract designed to manage a custom cryptocurrency token. The contract adheres to specific requirements, including the creation of a token, the ability to mint and burn tokens, and maintaining a balance for each address. This README will help you understand the project and how to use it.

## Getting Started
### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

When your'e there, you can start by creating a file by clinking on the "+" icon. Remember to save the file using a .sol extension.

Copy and paste thisd code into the file

pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "JUDE";
    string public tokenAbbreviation = "JOD";
    uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;


    
    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
    }
}
}

## Authors

@judefrancia

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
