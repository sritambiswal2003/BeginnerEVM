## MyToken Smart Contract

This is a simple Solidity smart contract named "MyToken" that represents a custom token on the Ethereum blockchain. The contract allows for token creation, minting, and burning functionalities.

### Contract Details

- SPDX-License-Identifier: MIT
- Solidity Version: 0.8.0

### Contract Overview

The "MyToken" contract has the following main features:

1. **Public State Variables**:
   - `tokenName`: A string variable that represents the name of the custom token.
   - `tokenAbbrv`: A string variable that represents the abbreviation of the custom token.
   - `totalSupply`: A uint256 variable that represents the total supply of the custom token.
   - `balances`: A mapping that associates token balances with their respective addresses.

2. **Constructor**: The constructor initializes the contract with initial values for `tokenName`, `tokenAbbrv`, and `totalSupply`. It also allocates the entire initial supply to the contract deployer (`msg.sender`) by updating their balance in the `balances` mapping.

3. **Functions**:
   - `mint(address _address, uint256 _value)`: A public function that allows the contract owner to mint new tokens and assign them to a specified `_address`. The `_value` parameter specifies the number of tokens to mint. The function increases the total supply and updates the balance of the specified address.

   - `burn(uint256 _value)`: A public function that allows users to burn (destroy) a specified amount of tokens from their own balance. The `_value` parameter specifies the number of tokens to burn. The function reduces the total supply and updates the user's balance accordingly.

### Important Notes

- This is a basic example of a custom token smart contract and is not intended for production use without proper testing and security considerations.
- The contract allows the contract owner to mint tokens, which should be used with caution to prevent unintended inflation of the token supply.
- Ensure that appropriate security measures and access controls are implemented before deploying this contract on the Ethereum blockchain.

### License
This code is licensed under the MIT License. You can find the license text in the SPDX-License-Identifier comment at the beginning of the contract.

Note: Ensure that you are using a compatible Solidity compiler version (0.8.18) or newer to compile and interact with this contract.
