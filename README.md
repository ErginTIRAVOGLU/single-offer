# Single Offer Token Exchange

A smart contract built on the Soroban platform that facilitates token pair trading between a single seller and multiple buyers.

# Build

stellar contract build 

- ℹ️  Build Summary:
-    Wasm File: target\wasm32-unknown-unknown\release\soroban_single_offer_contract.wasm
-    Wasm Hash: 95d8f4f1ea88ce2d93a639280f4293a8b75898296adfbbf5e3a3a49e8212316b
-    Exported Functions: 6 found
      • _
      • create
      • get_offer
      • trade
      • updt_price
      • withdraw
- ✅ Build Complete

# Deploy

stellar contract deploy --wasm target/wasm32-unknown-unknown/release/soroban_single_offer_contract.wasm --source-account alice --network testnet --alias single_offer

- ℹ️  Simulating install transaction…
- ℹ️  Signing transaction: 5bf82d03785cb84dca5d635d087d878a3d058c33bbe32dfc04e86f8ee5840ede
- 🌎 Submitting install transaction…
- ℹ️  Using wasm hash 95d8f4f1ea88ce2d93a639280f4293a8b75898296adfbbf5e3a3a49e8212316b
- ℹ️  Simulating deploy transaction…
- ℹ️  Transaction hash is ce2ae9a7762d10a980bb1029ba2045a906505f146812093ba171a6708a1ceb2d
- 🔗 https://stellar.expert/explorer/testnet/tx/ce2ae9a7762d10a980bb1029ba2045a906505f146812093ba171a6708a1ceb2d
- ℹ️  Signing transaction: ce2ae9a7762d10a980bb1029ba2045a906505f146812093ba171a6708a1ceb2d
- 🌎 Submitting deploy transaction…
- 🔗 https://stellar.expert/explorer/testnet/contract/CAT2AFJLGYKX2PF6UPRQR6JUCLJYRVDGZIRI2XI4CYNKOYUPRWBAG27K
- ✅ Deployed!
- CAT2AFJLGYKX2PF6UPRQR6JUCLJYRVDGZIRI2XI4CYNKOYUPRWBAG27K

## Overview

This contract implements a simple yet effective token exchange mechanism where a seller can create an offer to exchange one token for another at a specified price ratio. Multiple buyers can then trade with this offer without the need for order matching or complex exchange logic.

## Features

- **Single Seller Model**: One seller can create an offer for multiple buyers
- **Fixed Price Ratio**: Trading occurs at a predetermined price ratio
- **Minimum Amount Protection**: Buyers can specify a minimum amount to receive
- **Price Updates**: Seller can update the price ratio as needed
- **Withdrawal Function**: Seller can withdraw tokens from the contract

## Contract Structure

### Data Structures

- **DataKey**: Defines storage keys used in the contract
  - `Offer`: Stores the offer information

- **Offer**: Contains all the details about the trading offer
  - `seller`: Address of the seller
  - `sell_token`: Address of the token being sold
  - `buy_token`: Address of the token being bought
  - `sell_price`: Unit price for selling (per token)
  - `buy_price`: Unit price for buying (per token)

## Technical Details

- Built using the Soroban SDK for Stellar's smart contract platform
- Implemented with `#![no_std]` for efficient operation in blockchain environments
- Uses Rust's type system for safety and reliability
- Simple storage model with a single offer state

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
