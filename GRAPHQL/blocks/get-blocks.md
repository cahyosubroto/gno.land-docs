---
title: "Get Blocks with Specifict Time Range"
slug: "get-blocks"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:06:33 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 02:40:15 GMT+0000 (Coordinated Universal Time)"
---
In this use case, we will retrieve all blocks created within the specific time range. This will allow you to analyze the block creation frequency and transaction volume during that period.

## Sample Request

```graphql
query {
  blocks(filter: { from_time: "2024-08-01T00:00:00Z", to_time: "2024-08-01T12:00:00Z" }) {
    hash
    height
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
        "hash": "kADxL3doJ5B+VZmY8GWnpvhgFsFMlyMySIiat4heYsY=",
        "height": 508499,
        "time": "2024-08-01T00:00:23.381070565Z",
        "num_txs": 0,
        "total_txs": 9660
      },
      {
        "hash": "R0NdxLrByBmDA+OEwbVqxgmYWD+Q1BfUxJ3fwrnleL8=",
        "height": 509206,
        "time": "2024-08-01T11:59:17.914314107Z",
        "num_txs": 0,
        "total_txs": 9660
      }
    ]
  }
}
```

## Fields

The following fields are used and returned in this use case:

| **Component**                    | **Type**  | **Description**                                                                                                           |
| -------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `query`                          | `Object`  | Initiates a query to retrieve data from the blockchain.                                                                   |
| `blocks`                         | `Array`   | Retrieves a list of blocks within the specified time range.                                                               |
| `filter: { from_time, to_time }` | `Object`  | Filters the blocks based on the provided time range. The `from_time` is the start of the range, and `to_time` is the end. |
| `hash`                           | `String`  | The unique identifier (hash) of the block.                                                                                |
| `height`                         | `Integer` | The block’s position in the blockchain (increases sequentially).                                                          |
| `time`                           | `String`  | The timestamp of when the block was created.                                                                              |
| `num_txs`                        | `Integer` | The number of transactions included in the block.                                                                         |
| `total_txs`                      | `Integer` | The total number of transactions in the blockchain up to and including this block.                                        |
