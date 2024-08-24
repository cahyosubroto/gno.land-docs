---
title: "Get Transactions with Specific Messages"
slug: "get-all-transactions"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:04:25 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 02:55:49 GMT+0000 (Coordinated Universal Time)"
---
In this use case, we will retrieve all the blockchain transactions that contain`add_package` messages. This is useful for extracting key details such as the transaction creator, package name, and package path.

## Sample Query

```graphql
{
  transactions(
    filter: { message: {vm_param: {add_package: {}}}}
  ) {
    index
    hash
    block_height
    gas_used
    messages {
      route
      typeUrl
      value {
        __typename
        ... on MsgAddPackage {
          creator
          package {
            name
            path
          }
        }
      }
    }
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
        "block_height": 239,
        "gas_used": 447797,
        "messages": [
          {
            "route": "vm",
            "typeUrl": "add_package",
            "value": {
              "__typename": "MsgAddPackage",
              "creator": "g1jg8mtutu9khhfwc4nxmuhcpftf0pajdhfvsqf5",
              "package": {
                "name": "wgnot",
                "path": "gno.land/r/wgnot"
              }
            }
          }
        ]
      },
      {
        "index": 0,
        "hash": "hTkVl8eaFfqNLdhDgzFhHYPLit/XCNwZdPaL9o5fN/Y=",
        "block_height": 480688,
        "gas_used": 68997,
        "messages": [
          {
            "route": "vm",
            "typeUrl": "add_package",
            "value": {
              "__typename": "MsgAddPackage",
              "creator": "g1778y2yphxs2wpuaflsy5y9qwcd4gttn4g5yjx5",
              "package": {
                "name": "moodtest1",
                "path": "gno.land/r/michelle22/moodtest1"
              }
            }
          }
        ]
      }
    ]
  }
}
```

## Fields

The following fields are used and returned in this use case:

| **Field**                                             | **Type**  | **Description**                                                                                                     |
| ----------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `transactions`                                        | `Array`   | The root query to fetch transaction data from the blockchain.                                                       |
| `filter: { message: { vm_param: { add_package: {}}}}` | `Object`  | A filter applied to retrieve only those transactions that include `add_package` messages.                           |
| `index`                                               | `Integer` | The position of the transaction within its block.                                                                   |
| `hash`                                                | `String`  | The transaction's unique identifier (hash) is typically encoded in base64.                                          |
| `block_height`                                        | `Integer` | The block height that includes this transaction shows its location in the blockchain.                               |
| `gas_used`                                            | `Integer` | The amount of gas consumed by the transaction indicates the computational effort required.                          |
| `messages`                                            | `Array`   | A list of messages within the transaction.                                                                          |
| `route`                                               | `String`  | Indicates the module or route that processed the message, such as `vm` for virtual machine-related actions.         |
| `typeUrl`                                             | `String`  | Specifies the type of message, such as `add_package`, which describes the operation performed.                      |
| `value`                                               | `Object`  | The actual content of the message, including its type, creator, and associated package details.                     |
| `__typename`                                          | `String`  | Identifies the type of message, in this case, `MsgAddPackage`, which relates to adding a package to the blockchain. |
| `creator`                                             | `String`  | The address of the entity that created the package.                                                                 |
| `package.name`                                        | `String`  | The name of the package being deployed.                                                                             |
| `package.path`                                        | `String`  | The gno path of the package in the blockchain.                                                                      |
