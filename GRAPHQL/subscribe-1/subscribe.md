---
title: "Subscribe to New Blocks"
slug: "subscribe"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:04:54 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 03:58:03 GMT+0000 (Coordinated Universal Time)"
---
In this use case, we will subscribe to new blocks added to a blockchain in real time. This will allow you to receive updates instantly whenever a new block is created and provide important details about each block.

## Sample Query

```graphql
subscription {
  blocks(filter: {}) {
    height
    version
    chain_id
    time
    proposer_address_raw
  }
}
```

## Sample Response

```json
{
  "data": {
    "blocks": {
      "height": 538969,
      "version": "v1.0.0-rc.0",
      "chain_id": "test3",
      "time": "2024-08-23T08:16:00.022630609Z",
      "proposer_address_raw": "g1wyre4gr7n82ezfpdhg3nxypjy9cag9qpku5x6m"
    }
  }
}
```

## Fields

The following fields are used and returned in this use case:

| **Component**          | **Type**  | **Description**                                                   |
| ---------------------- | --------- | ----------------------------------------------------------------- |
| `subscription`         | `Object`  | Initiates a real-time subscription to receive continuous updates. |
| `blocks`               | `Object`  | Subscribes to all new blocks added to the blockchain.             |
| `height`               | `Integer` | The block’s position in the blockchain (increases sequentially).  |
| `version`              | `String`  | The version of the block indicates the protocol or software used. |
| `chain_id`             | `String`  | The unique identifier of the blockchain network.                  |
| `time`                 | `String`  | The timestamp of when the block was created.                      |
| `proposer_address_raw` | `String`  | The raw address of the node that proposed or validated the block. |
