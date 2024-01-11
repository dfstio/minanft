# MinaNFT

The MinaNFT project is an innovative Non-Fungible Token (NFT) platform that integrates the unique privacy features of the Mina blockchain with advanced AI technology. It's designed to redefine the NFT space by offering a range of functionalities that go beyond traditional NFT capabilities.

![MinaNFT structure](/images/structure.png)

Here are the key aspects of the MinaNFT project:

1. **Customized Avatar NFTs**: Users can create personalized avatar NFTs that serve as digital identifiers across social media platforms and in various corporate and contractual interactions.

2. **AI-Driven NFT Generation**: MinaNFT employs a user-friendly Telegram bot that enables users to generate unique NFTs by simply describing their avatar idea via text or voice message in any language. The AI technology then takes care of the creation process.

3. **Secure Repositories for Sensitive Information**: Avatar NFTs can securely store a range of both public and private information, including art, contracts, medical records, and proofs of ownership. This information is attached to the NFTs with verifiable proofs of authenticity.

4. **Privacy and Security**: For users and corporations prioritizing privacy, MinaNFT offers options to create custom NFTs through an offline CLI tool, ensuring that private content remains on the user's personal computer. A redacted version of documents can be shared, maintaining confidentiality while verifying authenticity.

5. **TypeScript Library for Integration**: MinaNFT provides a TypeScript library for third-party developers and corporate accounts, simplifying the process of deploying to the MINA blockchain and managing data proofs.

6. **Permanent Storage Options**: For NFTs featuring timeless art or significant documents, MinaNFT offers the option of permanent storage on Arweave, ensuring long-term preservation.

7. **Global Community Engagement**: MinaNFT aims to bring a broader community into the NFT space, addressing challenges of identity, privacy, and on-chain and off-chain verifiability of diverse NFT content.

8. **Architecture**: The project's architecture includes key contracts on the Mina blockchain, a frontend, backend API, Telegram bot, MinaNFT offline CLI tool, and integration library, all working in tandem to provide a seamless user experience.

In essence, MinaNFT is about expanding the utility of NFTs beyond digital art, transforming them into versatile tools for identity representation and secure content sharing in the digital realm. It leverages the strengths of the Mina blockchain and AI to offer enhanced privacy, security, and functionality.

## Features

### Contracts library and data structures

- [MinaNFTContract](https://docs.minanft.io/api/class/minanftcontract/) for NFT
- MinaNFTNameServiceContract for Name Service
- MinaNFTMetadataUpdate ZkProgram for metadata updates using Merkle Map proofs
- RedactedMinaNFTMapCalculation for redacted Merkle Maps proofs
- RedactedMinaNFTTreeCalculation for redacted Merkle Tree proofs
- MinaNFTVerifier and MinaNFTTreeVerifier for verification of redacted map and tree proofs
- MinaNFTVerifierBadge for assigning badges to NFTs
- Escrow for NFT transfers through the escrow mechanism
- NFTMintData, MintData, Metadata, MetadataMap, MetadataWitness, MetadataUpdate, MetadataTransition, Storage, Update, EscrowTransfer, EscrowApproval data structures to be used in contracts

## Documentation

https://docs.minanft.io

https://github.com/dfstio/minanft-docs

## Website

https://minanft.io

https://github.com/dfstio/minanftio

## Telegram bot and API

https://t.me/minanft_bot

https://github.com/dfstio/minanft-api

## Library

https://www.npmjs.com/package/minanft

https://github.com/dfstio/minanft-lib

## Example

https://github.com/dfstio/minanft-lib-example

## MinaNFT CLI tool

https://github.com/dfstio/minanft-cli
