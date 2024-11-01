## Hashi template - Foundry edition

This folder demonstrates a basic use case for Hashi using Foundry. For more details about Foundry, see their [documentation](https://book.getfoundry.sh/getting-started/first-steps).

# Develoment

## Contracts

The `Sender` and `Receiver` contracts demonstrate how to dispatch messages using Hashi.

The `Sender `contract on the source chain interacts with the `Yaho` contract, specifying the oracles (reporters and adapters) required for message dispatching.
On the target chain, the `Receiver` contract updates the message once the threshold is met by the adapters.
For a detailed example using Sepolia as the source chain and Chiado as the target chain, see `contracts/SepoliaSender.sol` and `contracts/ChiadoReceiver.sol`.

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

Configure parameters in .env. Run script

```shell
$ forge script script/$ContractName.s.sol: --rpc-url <your_rpc_url> --private-key <your_private_key> --broadcast --verify
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
