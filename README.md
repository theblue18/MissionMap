# MissionMap Beta v2 Testing Guide

Welcome to the MissionMap Beta testing guide. This document outlines the key features and functionalities that need to be tested in the latest version of MissionMap. Your thorough testing and feedback are essential in refining and enhancing the user experience.

## Beta2 link: [https://beta2.missionmap.io/](https://beta2.missionmap.io/)

## Login Methods And Responsive

- Only Support Wallets: Metamask, Coinbase Wallet,... Note that currently, social logins, email, and phone logins are not supported.
- Currently, MissionMap only supports a web interface on desktop and does not yet have responsive support for mobile phones and tablets.

## For Mission Makers

### Creating and Managing Spaces

- Create New Space: Navigate to 'For Projects' to create a new Space.
Edit Space: Access and modify the details of your Space.
- Community Creation: Within a Space, you can create a global Community or a Region Community specific to your area (e.g., United States). This includes editing functionalities.
- Campaign Creation: Set up Campaigns within a Community. Customize tasks, rewards, and campaign rules.

### Create Onchain Tasks

#### Supported Networks
- Network Compatibility: We currently support a limited range of chain networks for OnChain mission tracking, including Base, Base Goerli, ETH, and ETH Sepolia.
- Tracking Transactions: Our system utilizes Alchemy to fetch transaction lists. Therefore, for networks like Base and Base Goerli, we can only track transactions involving tokens such as ERC20, ERC721, ERC1155, and Specialnft. For more information on this, please refer to the Alchemy documentation here: [Achemy GetAssetTransfers](https://docs.alchemy.com/reference/alchemy-getassettransfers).

- Additional Tracking: Besides the specific tokens mentioned, MissionMap Beta 2.0 is also capable of tracking external and internal transactions of a SmartContract.

#### Example 1: Swap Token

  - Task Description: Execute a token swap from BEG to USDC on BeagleSwap on the Base Goerli network.
  - Link: https://beagleswap.xyz/swap
  - Network: Base Goerli
  - Smart Contract Address: 0x8e8214cdcaa691983a87264db7ab83c399fe7f3b
  - Function: multicall(uint256,bytes[])

#### Example 2: Bridge ETH
  - Task Description: Bridge ETH from ETH Sepolia to Scroll Sepolia using Scroll Official Bridge.
  - Link: https://sepolia.scroll.io/bridge
  - Network: ETH Sepolia
  - Smart Contract Address: 0x13FBE0D0e5552b8c9c4AE9e2435F38f37355998a
  - Function: depositETH(uint256,uint256)

### Testing Location Tasks
Location Task: Tasks are considered completed only if the user's current location is within the region of the Community. In global communities, the task is always marked as successful.

## For Mission Takers
### Exploring and Participating in Missions
- Browse Spaces: View a list of Spaces and details of a specific Space.
- Community Engagement: View and engage with Communities, access the leaderboard, and see your collected points.
- Campaign Interaction: View Campaigns, their details, and participate.
Complete tasks, verify rules, and claim points.


### Notes for participating in tasks and rules:
- Photo and Video Tasks require Mission Maker confirmation, which is currently unavailable. Thus, these tasks cannot be successfully verified yet.
- For Onchain Tasks like Example 1: Swap Token. If you don't already have BEG, you can swap Base Goerli ETH for BEG. Then, swapping BEG for USDC will complete the task. Faucet Base Goerli here: [Base Goerli](https://coinbase.com/faucets/base-ethereum-goerli-faucet)
- For rules requiring a Gitcoin Passport Score, please follow this link: [Gitcoin Passport](https://passport.gitcoin.co/), and follow the steps to obtain your Score information.

## Feedback and Reporting
Your input is invaluable to us. While testing, please provide feedback on functionality, user experience, and any issues encountered. We aim to make MissionMap a seamless and engaging platform for both Mission Makers and Takers.

Thank you for contributing to the development and improvement of MissionMap Beta.

## License
This guide is subject to updates as MissionMap evolves.
[MIT](https://choosealicense.com/licenses/mit/)
