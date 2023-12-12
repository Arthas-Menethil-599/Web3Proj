# SOLYANKA DAO 

[SOLYANKA DAO](https://solyanka-dao.vercel.app/) is a decentralized autonomous community (DAO) designed for voting in the blockchain. The smart contract was written in Hardhat, and the front-end was written in React using the Ant Design library for the interface and Wagmi/Ethers/RainbowKit for working with the blockchain.


## Features

- Create a vote with title, candidates, quorum and duration.
- User registration to participate in voting.
- View the list of votes.
- Editing user-created votes.
- Notifications about transaction status.

## Setup instructions

1. Clone the repository:

```
git clone https://github.com/SweetBubalehj/SOLYANKA-DAO.git
```

2. Install dependencies for hardhat (to work with the contract):

```
cd .\DAO-dapp\app-hardhat\
npm install
```

3. Install dependencies for react:

```
cd .\DAO-dapp\app-react\
npm install
```

4. Run the react project:

```
npm start
```


## Main components


### Back-End(web3)

#### Main contracts
- `SBToken.sol`: SBT token for working with user accounts, as well as for confirming KYC and limiting access between users by adding moderators.
- `Staking.sol`: implements the possibility of depositing $SLK tokens, with subsequent receipt of rewards.
- `VotingFactory.sol`: the main contract for creating votes.
- `SolyankaToken.sol`: the main ERC20 token used in the DAO.

#### Frameworks

- Hardhat

### Front-End

#### App.js

`App.js` contains the basic structure of the application, including the layout, header with menu, logo, connect button and content sections.

#### contracts

The `contracts` folder contains the ABIs of the `factoryContract`, `btContract`, `stakingContract`, `tokenContract`, `tokenWeightedContract`, `votingContract` contracts that are used in the application. ABI allows you to interact with contracts from the blockchain.

#### Components

The `components` folder contains the main components of the application, such as registration, forms for creating votes, editing and participation, as well as the list of votes itself.

- `CreateVotingForm`: Form for creating a new vote.
- `CreateIdentity`: User registration form.
- `VotingList`: A component that displays a list of available votes, interacting with them using a modal window.
- `VotingSettings`: Form for the creator of the vote to edit it.
- `VotingModeration`: Form for moderating votes, allows the moderator to change their name.

#### Utils

The `utils` folder contains utility functions used in various parts of the application, such as user validation.

- `isAdmin`: checking the user for administrator rights.
- `isIdentified`: checking the user for registration.
- `IsKYC`: user identification verification.
- `isModerator`: checking the user for moderator rights.
- `getRandomGradient.js`: to get the gradient.

## Using

1. Connect to your wallet by clicking the "Connect" button in the upper right corner.
2. Create a vote by filling out the "Create Voting" form.
3. Create an identity by filling out the "Create Identity" form.
4. View the list of active votes in the "Voting List" section.
5. Manage polls by creating them, voting, changing their parameters and monitoring the status of transactions.

> - SBT: 0xF840C81dB1958227c4021143Dd7E949c881C3600
> - ERC20: 0xC97F0A883BcBf2338bAc5db23025ec00E568c95a
> - Staking: 0x844F750EC4A4Af759E68713E8c776bd8dEB778f3
> - Factory: 0xa7187beb237cf6b0a2D50714C948b89e413e0cE4
