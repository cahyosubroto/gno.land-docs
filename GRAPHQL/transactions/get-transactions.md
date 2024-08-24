---
title: "Get Transaction Status"
slug: "get-transactions"
excerpt: ""
hidden: false
createdAt: "Sat Aug 24 2024 03:00:25 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 03:51:26 GMT+0000 (Coordinated Universal Time)"
---
In this use case, we will retrieve all the transaction statuses.

## Sample Query

```graphql
query {
  transactions(filter: { }) {
    index
    hash
    success
    block_height
  }
}

```

## Sample Response

```json
{
  "data": {
    "transactions": [
      {
        "index": 0,
        "hash": "1Ozj5CQWm1H2Oy8tnB8Ds8KcdebGmgTRwSPBSAxX2Zc=",
        "success": false,
        "block_height": 239
      },
      {
        "index": 0,
        "hash": "x8M2926jox/SvdB0eIjBh5/e+koQB3cj/tsytarjYC0=",
        "success": false,
        "block_height": 241
      },
      {
        "index": 0,
        "hash": "723ktcvUS9WEGKpnpONNVRqqosmHm3odEKk8Pb+8CSA=",
        "success": true,
        "block_height": 250
      },
      {
        "index": 0,
        "hash": "Z9vT1HeegzjLCN4SVtYKDqBEmfH07+k3q6qbemBy0Dw=",
        "success": false,
        "block_height": 260
      },
      {
        "index": 0,
        "hash": "svmcN9ofIsy8O8k6le3aLVOvINDx4Z2eZPdU1P5nHfg=",
        "success": false,
        "block_height": 262
      }
    ]
  }
}
```

## Fields

The following fields are used and returned in this use case:

| **Field**      | **Type**  | **Description**                                                                         |
| -------------- | --------- | --------------------------------------------------------------------------------------- |
| `transactions` | `Object`  | Specifies the range of block heights to filter the transactions returned by the query.  |
| `index`        | `Integer` | The position of the transaction within its block.                                       |
| `hash`         | `String`  | The unique identifier (hash) of the transaction.                                        |
| `success`      | `Boolean` | Indicates whether the transaction was successfully processed (`true`) or not (`false`). |
| `block_height` | `Integer` | The height of the block in which the transaction was included.                          |
