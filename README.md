# User-Referral-Rewards-Tokens
# Referral Program Smart Contract

This Solidity smart contract implements a referral program where users can refer others and earn token rewards. The contract is managed by an owner who assigns referrals and distributes rewards manually.

## Features
- Assign referrers to users
- Distribute token rewards to referrers
- Prevent duplicate referrals and reward claims
- Check reward balance for any user

## Contract Details
- The contract does not use imports or constructors.
- All functions are controlled by the contract owner.
- Rewards are stored in a mapping and can be checked by users.

## Functions
### `setReferrer(address user, address _referrer)`
Assigns a referrer to a user (Only callable by the owner).

### `distributeReward(address user)`
Distributes a token reward to the referrer when a referred user qualifies (Only callable by the owner).

### `checkReward(address user) → uint256`
Returns the total rewards earned by a referrer.

## Usage
1. Deploy the contract to an Ethereum-compatible blockchain.
2. The owner assigns referrers using `setReferrer`.
3. The owner distributes rewards using `distributeReward`.
4. Referrers can check their rewards using `checkReward`.

## Notes
- Users cannot refer themselves.
- Each user can only have one referrer.
- The owner must manually distribute rewards.

## License
This project is open-source and available for use under the MIT License.

