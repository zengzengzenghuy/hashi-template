# Hashi template - Hardhat edition

This folder demonstrates a basic use case for Hashi using Hardhat. For more details about Hardhat, see their [documentation](https://hardhat.org/docs).

```
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat ignition deploy ./ignition/modules/$ContractName.js --network $Network --verify
```

# Development

## Setup

Install dependencies:

```
npm install
```

## Deployment

Copy the example environment file and configure it:

```
cp .env.example .env
```

Adjust deployment parameters in the .env file as needed. To add new networks, configure them in `hardhat.config.js`.

Deploy the contract:

```
npx hardhat ignition deploy ./ignition/modules/$ContractName.js --network $Network --verify
```

## Contracts

The `Sender` and `Receiver` contracts demonstrate how to dispatch messages using Hashi.

The `Sender `contract on the source chain interacts with the `Yaho` contract, specifying the oracles (reporters and adapters) required for message dispatching.
On the target chain, the `Receiver` contract updates the message once the threshold is met by the adapters.
For a detailed example using Sepolia as the source chain and Chiado as the target chain, see `contracts/SepoliaSender.sol` and `contracts/ChiadoReceiver.sol`.
