# MyToken

This is a simple ERC-20 token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

## Requirements

1. The contract has public variables that store the details about the coin:
   - `toknName`: A string representing the name of the token.
   - `toknAbbrv`: A string representing the abbreviation of the token.
   - `totlSupply`: An unsigned integer representing the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `blnc`: A mapping that associates addresses with their corresponding token balances.

3. The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `position`: The address to which the tokens will be minted.
     - `val`: The amount of tokens to be minted.
   - Actions:
     - Increase the `totlSupply` by `val`.
     - Increase the balance of the `position` by `val`.

4. The contract has a `burn` function that decreases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `position`: The address from which the tokens will be burned.
     - `val`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `position` is greater than or equal to `val`.
     - If true, decrease the `totlSupply` by `val`.
     - Decrease the balance of the `position` by `val`.

## Usage

1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `position`: The address to which the tokens will be minted.
       - `val`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `position`: The address from which the tokens will be burned.
       - `val`: The amount of tokens to be burned.

## Authors

Sanyam Singh

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.

