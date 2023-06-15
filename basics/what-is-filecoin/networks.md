---
description: >-
  The Filecoin network has several different networks for testing, staging, and
  production purposes. This page contains information on available networks.
---

# Networks

### Mainnet

[Mainnet](https://docs.filecoin.io/networks/mainnet/details/) is the live production network that all nodes on the Filecoin network are connected to. It never resets.

### Testnets

Test networks, or testnets, are version of the Filecoin network that attempt to simulate various aspects of the Filecoin mainnet. Since they are for testing they should not be used for production applications or services.

#### Calibration

[Calibration](https://docs.filecoin.io/networks/calibration/details/) testnet is the most realistic simulation of the mainnet, where prospective storage providers can experience more realistic sealing performance and hardware requirements due to the use of final proofs constructions and parameters, and prospective storage clients can store and retrieve real data on the network. Clients can participate in deal-making workflows and storage/retrieval functionality. It also has the same sector size as the mainnet.

* [Public endpoint](https://api.calibration.node.glif.io/rpc/v0)
* [Blockchain explorer](https://calibration.filscan.io/)
* [Faucet](https://faucet.calibration.fildev.network/)

#### Spacenet

[Spacenet](https://docs.filecoin.io/networks/spacenet/details/) is a Filecoin testnet that’s been modified to support Interplanetary Consensus (IPC). It aims to provide developers with a testbed to deploy their FVM use cases and innovate with new Web3 applications that leverage IPC subnets and the high-performance consensus provided by the Mir framework and the Trantor BFT consensus protocol.

* [Details](https://docs.filecoin.io/networks/spacenet/details/)
* [Public endpoint](https://docs.filecoin.io/networks/spacenet/rpcs/)
* [Faucet](https://docs.filecoin.io/networks/spacenet/get-test-tokens/)
