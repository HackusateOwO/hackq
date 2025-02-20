# Daily Login Rewards Smart Contract

## Overview
This Solidity smart contract implements a simple daily login rewards system. Users can log in once per day to receive a predefined number of reward tokens.

## Features
- Users can log in once per day to claim rewards.
- Stores the last login timestamp for each user.
- Keeps track of the accumulated rewards for each user.
- Emits an event when a user logs in.

## Smart Contract Details

### State Variables
- `lastLogin`: A mapping that stores the last login timestamp of each user.
- `rewards`: A mapping that keeps track of the total rewards earned by each user.
- `rewardAmount`: The fixed amount of tokens awarded per daily login (default: 10).

### Functions
#### `login()`
- Allows a user to claim their daily reward.
- Ensures the user can only log in once per day.
- Updates the `lastLogin` timestamp and increments the reward balance.
- Emits a `LoggedIn` event.

#### `checkRewards(address user) → uint256`
- Returns the total rewards earned by the specified user.

## Deployment & Usage
### Deploying the Contract
1. Use **Remix IDE** or **Hardhat** to deploy the contract.
2. Compile using Solidity `0.8.0` or later.
3. Deploy on a blockchain (testnet or mainnet) using MetaMask.

### Interacting with the Contract
- Call `login()` once per day to claim rewards.
- Use `checkRewards(address user)` to view the accumulated rewards.

## License
This project is licensed under the **MIT License**.

