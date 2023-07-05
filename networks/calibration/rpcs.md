---
description: Public RPC endpoints are available for the Calibration testnet.
---

# RPCs

These endpoints are limited to [read-only Filecoin JSON RPC API calls](https://docs.filecoin.io/reference/json-rpc/introduction/) and [`MPoolPush`](https://docs.filecoin.io/reference/json-rpc/mpool/#mpoolpush) for sending messages that have already been signed.

## [ChainupCloud](https://cloud.chainup.com)

* HTTPS: `https://filecoin-calibration.chainup.net/rpc/v1`
* WebSocket: `wss://filecoin-calibration.chainup.net/rpc/v1`
* [ChainupCloud documentation](https://docs.chainupcloud.com/blockchain-api/filecoin/public-apis)

## [Glif](https://glif.io)

Please note that publicly available hosted endpoints **only guarantee 2000 of the latest blocks.**

* HTTPS: `https://api.calibration.node.glif.io/rpc/v1`
* WebSocket: `wss://wss.calibration.node.glif.io/apigw/lotus/rpc/v1`
*   Lotus lite-node command

    ```shell
    FULLNODE_API_INFO=wss://wss.calibration.node.glif.io/apigw/lotus lotus daemon --lite
    ```

    When using a lite-node, omit `/rpc/v1` from Glif’s WebSocket address.

* [Glif documentation](https://hosting.glif.io/)
