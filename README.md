# SOLIDTY TOKEN SMART CONTRACT

This Solidity Contract defines a simple token contract with minting and burning functionalities.The Contract allows us for the creation and destruction of tokens.
    [VIDEO EXPLAINATION OF THIS PROJECT](https://www.loom.com/share/2f9b466a046e41e68a28e9c80e0533b2?sid=56a526eb-d976-4233-b1c9-62d122998011)

## Description

The MyToken contract implements the functions to handle the token on Ethereum Blockchain. It includes
1. Public Variables to store the Token's Details which Includes TokenName, TokenAbbreviation, TotalSupply.
2. A Mapping is done for address to uint which is named balances.
3. A mint function is added to create new tokens and add them to specified address.
4. A burn function is added to destroy tokens from a specified address and ensuring that address has enough balance.


## Getting Started

### Installing
Remix - An Online Solidity IDE is used to run this program.

### Executing program
1. Go to Remix Website at [REMIX IDE](https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.25+commit.b61c2a91.js)
2. Create a NEW file there by clicking on the "+" icon on the left hand sidebar.
3. Name the file as you want and save it with .sol extension
4. Copy the code Given Below: 
```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;



contract MyToken {
     
    // public variables here
    string public TokenName ="SOLIDITY PROJECT";
    string public TokenAbbreviation="SOL";
    uint public TotalSupply=0; 

    // mapping variable here
    mapping (address =>uint ) public balances;

    // mint function
    function mint (address _tokenaddress, uint _amount) public {
        TotalSupply += _amount;
        balances[_tokenaddress]+=_amount;
    }
    // burn function
    function burn (address _tokenaddress, uint _amount) public {
        if (balances[_tokenaddress]>=_amount){
        TotalSupply -= _amount;
        balances[_tokenaddress]-=_amount;
    }

}
}
```
4. To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the
   "Compile MyToken.sol" button.
5. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the MyToken contract from the dropdown menu, and then click on the "Deploy" button.
6. Once the contract is deployed, you can interact with it by calling the mint and burn functions.
7. Now Input the Necessary Parameters and execute the Functions.


## Help
If you encounter any Issue, ensure the following:
  1.The Compiler Version of Solidity is set Correctly.
  2.The address used in function calls is valid.
For any other help , use remix documentation.

## Authors
Metacrafter UDAY CHOPRA ---->
[UDAY CHOPRA](https://www.linkedin.com/in/uday-chopra-86701b2b0/)

## License
This project is licensed under the MIT License
