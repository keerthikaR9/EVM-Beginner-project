# MyToken Smart Contract

The MyToken smart contract is a simple Solidity contract that allows for the creation, minting, and burning of tokens. It is designed to be a basic representation of a token with functionalities to mint new tokens and burn existing ones, while maintaining a ledger of token balances for different addresses.

## Contract Details

The contract includes the following public variables:

- `TokenName`: A string representing the name of the token, set to "Shibainu" in this example.
- `TokenAbr`: A string representing the abbreviation or symbol of the token, set to "SHIB" in this example.
- `TotalSupply`: An unsigned integer representing the total supply of the token, initially set to 0.

Additionally, the contract includes a mapping to keep track of the token balances for different addresses. The mapping, `balance`, associates addresses (type `address`) with their respective token balances (type `uint`).

## Mint Function

The `mint` function allows for the creation of new tokens. It takes two parameters:

- `_address`: The address to which the new tokens will be minted.
- `_value`: The amount of tokens to mint and add to the specified address.

When `mint` is called, it increases the total supply of tokens by the specified `_value` and adds the same amount to the balance of the `_address`. This function can be used to create new tokens and distribute them to specific addresses.

## Burn Function

The `burn` function allows for the burning (destruction) of existing tokens. It also takes two parameters:

- `_address`: The address from which tokens will be burned.
- `_value`: The amount of tokens to burn from the specified address.

Before burning tokens, the function checks if the balance of the `_address` is greater than or equal to the specified `_value`. If this condition is met, it deducts the specified `_value` from both the total supply and the balance of the `_address`. This function is used to reduce the total supply and remove tokens from specific addresses.

## Usage

You can deploy the MyToken contract on the Ethereum blockchain and interact with it using Ethereum wallets and smart contract development platforms. Here are some common use cases:

- **Creating Tokens**: Use the `mint` function to create and distribute tokens to specific addresses.
- **Destroying Tokens**: Use the `burn` function to remove tokens from circulation by burning them from specific addresses.
- **Checking Balances**: You can query the balance of any address using the `balance` mapping.
- **Viewing Token Information**: You can retrieve the token name, symbol, and total supply using the respective public variables (`TokenName`, `TokenAbr`, and `TotalSupply`).

## Author

Keerthika R

## Licence

This project is licensed under the MIT License - see the LICENSE.md file for details.