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

### Contracts library

- [MinaNFTContract](https://docs.minanft.io/api/class/minanftcontract/) for NFT
- [MinaNFTNameServiceContract](https://docs.minanft.io/api/class/minanftnameservicecontract/) for Name Service
- [MinaNFTMetadataUpdate](https://docs.minanft.io/api#MinaNFTMetadataUpdate) ZkProgram for metadata updates using Merkle Map proofs
- [RedactedMinaNFTMapCalculation](https://docs.minanft.io/api#RedactedMinaNFTMapCalculation) for redacted Merkle Maps proofs
- [RedactedMinaNFTTreeCalculation](https://docs.minanft.io/api#RedactedMinaNFTTreeCalculation20) for redacted Merkle Tree proofs
- [MinaNFTVerifier](https://docs.minanft.io/api/class/minanftverifier/) and MinaNFTTreeVerifier for verification of redacted map and tree proofs
- [MinaNFTVerifierBadge](https://docs.minanft.io/api/class/minanftverifierbadge/) for assigning badges to NFTs
- [Escrow](https://docs.minanft.io/api/class/escrow/) for NFT transfers through the escrow mechanism
- [NFTMintData](https://docs.minanft.io/api/class/nftmintdata/), [MintData](https://docs.minanft.io/api/class/mintdata/), [Metadata](https://docs.minanft.io/api/class/metadata/), MetadataMap, MetadataWitness, MetadataUpdate, MetadataTransition, Storage, Update, EscrowTransfer, EscrowApproval data structures to be used in contracts

### Data that can be put into NFT

- **Keys and Values:** strings up to 30 characters and Fields, written as Fields
- **Texts:** texts of any length, written as Field arrays
- **Files:** text, image, word, any other formats, including audio, video, PDF, binary. Written as two Merkle Trees: one with metadata and the other with file data: 30 bytes per Field for binary files, one character per Field for text files, and one pixel per Field for image files
- **Maps:** any collection of the types above grouped together.
- All the data can be marked as public or private

### Proving and verifying the data

- Proving and verifying key-value pairs
- Proving and verifying the texts, including redacted
- Proving and verifying the text and binary files as a whole file using SHA3-512
- Proving and verifying the redacted text and word files (some characters can be redacted by using masks)
- Proving and verifying the redacted PNG image files (some pixels can be redacted by using masks)

### Frontend minanft.io

- [Explore](https://minanft.io/explore) all the NFTs
- [Explore](https://minanft.io/posts) all the posts
- [Create](https://minanft.io/create) NFTs and posts
- [Prove](https://minanft.io/proofs) public and private key-value pairs
- [Verify](https://minanft.io/proofs) public and private key-value pairs off-chain and on-chain
- [CLI tool helpers](https://minanft.io/tools)
- [Corporate onboarding](https://minanft.io/corporate)
- [Billing reports](https://minanft.io/corporate/billing)

### API

- [NFT name reservation](https://docs.minanft.io/api/class/api/#reserveName)
- [NFT name lookup](https://docs.minanft.io/api/class/api/#lookupName)
- [NFT minting](https://docs.minanft.io/api/class/api/#mint)
- [Indexing NFT for frontend](https://docs.minanft.io/api/class/api/#indexName)
- [Creation of the post](https://docs.minanft.io/api/class/api/#post)
- [Creation and verification of the proofs, minting and sending transaction](https://docs.minanft.io/api/class/api/#proof)
- [Retrieving proof calculation results](https://docs.minanft.io/api/class/api/#waitForJobResult)
- [Getting billing reports](https://docs.minanft.io/api/class/api/#queryBilling)

### Telegram bot

- [Creates simple NFTs](https://t.me/minanft_bot?start) (name + image) in a lite mode. The bots always start in lite mode and automatically switch to the full mode after the user has minted the first NFT.
- In full mode:
  - Generates images using a DALL-E model
  - Explain to a user how to create NFTs, posts, and key-value pairs for NFTs
  - Accepts and stores any files uploaded by the user for adding to the NFT or post
  - List NFTs of the user
  - List files of the user
  - List keys of the NFTs
  - Adds private and public key-value pairs to the NFT
  - Prove private and public key-values pairs of the NFT
  - Verifies proofs of the private and public key-values pairs of the NFT
- Accepts text messages and voice messages
- In voice mode, send voice messages to the user. The communication can be fully in voice in voice mode.

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
