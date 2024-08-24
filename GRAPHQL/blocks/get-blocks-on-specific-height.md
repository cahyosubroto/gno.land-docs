---
title: "Get Blocks with Specific Height"
slug: "get-blocks-on-specific-height"
excerpt: ""
hidden: false
createdAt: "Sat Aug 24 2024 02:40:36 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 02:55:32 GMT+0000 (Coordinated Universal Time)"
---
In this use case, we will retrieve all blocks within the specific block heights, along with each block's hash, height, version, chain ID, time of creation, and the number of transactions in it.

## Sample Request

```graphql
query {
  blocks(filter: { from_height: 100, to_height: 105 }) {
    hash
    height
    version
    chain_id
    time
    num_txs
    total_txs
  }
}

```

## Sample Response

```json
{
  "data": {
    "blocks": [
      {
        "hash": "i8BZLNpliBq5bBC10Wgn0/dSS8wCQGva23whFZs26Ck=",
        "height": 100,
        "version": "v1.0.0-rc.0",
        "chain_id": "test3",
        "time": "2023-08-18T13:22:21.152657062Z",
        "num_txs": 0,
        "total_txs": 2
      },
      {
        "hash": "5bknPVaCxLD7pwfwqFVS1mb4IZ30zrOYrzfguVvDgeo=",
        "height": 101,
        "version": "v1.0.0-rc.0",
        "chain_id": "test3",
        "time": "2023-08-18T13:23:22.16866702Z",
        "num_txs": 0,
        "total_txs": 2
      },
      {
        "hash": "+dT505l4Gm50ctANd1wVPBnWwpYgN0d/eDUXikpI76A=",
        "height": 102,
        "version": "v1.0.0-rc.0",
        "chain_id": "test3",
        "time": "2023-08-18T13:24:23.187265702Z",
        "num_txs": 0,
        "total_txs": 2
      },
      {
        "hash": "l/MCUFkeKQ9ny67f5w1axEdSLl8H49rT9rzuxRnay2Y=",
        "height": 103,
        "version": "v1.0.0-rc.0",
        "chain_id": "test3",
        "time": "2023-08-18T13:25:24.203423371Z",
        "num_txs": 0,
        "total_txs": 2
      },
      {
        "hash": "J1YL9AKsWeEnB7rpx0zIgfVXcxAOnKxUO4o8+OXOTDo=",
        "height": 104,
        "version": "v1.0.0-rc.0",
        "chain_id": "test3",
        "time": "2023-08-18T13:26:25.218614918Z",
        "num_txs": 0,
        "total_txs": 2
      }
    ]
  }
}
```

## Fields

The following fields are used and returned in this use case:

| **Field**                            | **Type**  | **Description**                                                                                                                                            |
| ------------------------------------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `query`                              | `Object`  | Initiates a query to retrieve data from the blockchain.                                                                                                    |
| `blocks`                             | `Array`   | Retrieves a list of blocks within the specified block heights.                                                                                             |
| `filter: { from_height, to_height }` | `Object`  | Specifies the range of block heights to filter the blocks returned by the query. The `from_height` is the start of the height, and `to_height` is the end. |
| `hash`                               | `String`  | The unique identifier (hash) of the block.                                                                                                                 |
| `height`                             | `Integer` | The block’s position in the blockchain (increases sequentially).                                                                                           |
| `version`                            | `String`  | The version of the block indicates the protocol or software version used to create the block.                                                              |
| `chain_id`                           | `String`  | The unique identifier of the blockchain network to which the block belongs.                                                                                |
| `time`                               | `String`  | The timestamp of when the block was created.                                                                                                               |
| `num_txs`                            | `Integer` | The number of transactions included in the block.                                                                                                          |
| `total_txs`                          | `Integer` | The total number of transactions in the blockchain up to and including this block.                                                                         |
