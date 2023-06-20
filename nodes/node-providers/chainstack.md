---
description: >-
  Instead of manually managing and running a node, developers can use
  third-party node providers like Chainstack to execute transactions.
---

# Chainstack

The ChainStack RPC API, maintained by [Chainstack Labs](https://chainstack.com/), provides high-performance testnet nodes for Filecoin builders, especially for applications built on the Filecoin Virtual Machine. The ChainStack RPC API provides both a standard endpoint and a WebSocket endpoint. For further information, see the [official page](https://chainstack.com/labs/#filecoin)

## HTTP endpoints

```plaintext
https://filecoin-calibration.chainstacklabs.com/rpc/v0
```

## Web socket endpoints

```plaintext
wss://ws-filecoin-calibration.chainstacklabs.com/rpc/v0
```

## Curl example

```shell
curl -X POST 'https://filecoin-calibration.chainstacklabs.com/rpc/v0' \
    -H 'Content-Type: application/json' \
    --data '{"jsonrpc":"2.0","id":1,"method":"Filecoin.ChainHead","params":[]}'
```
