# MyToken Project
A simple Ethereum smart contract for minting and burning tokens.

# Description
MyToken is a simple contract implemented in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This contract permits the generation of unique tokens with designated names and acronyms. It allows for minting new tokens and burning existing tokens and tracking the balances of token holders.

## Getting Started
### Installing
Interacting with the MyToken contract requires no installation as it is deployed on Remix IDE, a web-based IDE for Ethereum smart contract development.

### Executing 
1. Open Remix: Navigate to the Remix IDE in your web browser.

 
2. Create a New File:
   
    * In the left panel, click on the "+" icon to create a new file.

    * Name the file ``` myToken.sol```.
      

4. Copy the Contract Code:
   
    * Copy and paste the contract code into ```myToken.sol```.
    ```javascript
      pragma solidity 0.8.18;
      contract MyToken {
      string public name = "MyToken";
      string public symbol = "MTK";
      uint public totalSupply = 0;
      
      mapping(address => uint) public balances;
      
      function mint(address _to, uint _value) public {
        totalSupply += _value;          
        balances[_to] += _value;        
      }
   
      function burn(address _from, uint _value) public {
        if(balances[_from]>= _value){  
        totalSupply -= _value;          
        balances[_from] -= _value; 
        }    
       }
      }

5. Compile the contract

    * Compile the contract by selecting the appropriate Solidity version (0.8.18 in this case).

6. Deploy the contract
   
   * Deploy the contract using the Remix deploy and run transactions plugin.

7. Interact with the contract
   
   * After deployment, you can interact with the contract in the left-hand sidebar.
   * Click on mint funtion to mint tokens to specific addresses.
   * Click in burn function to burn tokens from specific addresses.

## Help

If you encounter any issues while using Remix IDE or have questions about the MyToken contract functionality, refer to the Remix documentation or seek support from the Ethereum developer community.

## Author 

Sushma

