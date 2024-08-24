---
title: "GraphQL API Overview"
slug: "graphql-api"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 07:40:50 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 05:28:26 GMT+0000 (Coordinated Universal Time)"
---
`tx-indexer` offers GraphQL API to retrieve and manage data from the blockchain. Once you run the `tx-indexer` you can access the following feature:

- **GraphQL API Playground**: Available at `http://localhost:8546/graphql`, this interface allows you to explore and test the API. It also includes comprehensive documentation of the root and schema types.
- **GraphQL Endpoint**: Accessible at `http://localhost:8546/graphql/query` that supports standard queries for transactions, blocks, and subscriptions for real-time events.

## Access the GraphQL Feature

To access the feature, follow the steps below:

1. Run the installed `tx-indexer` on your local machine.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/07322843d6108a566c723e4b70192883b464968f3418e5f822d0fa4506965339-Screenshot_2024-08-23_171310.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


2. Navigate to the `http://localhost:8546/graphql` to access the playground.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/423673c2dd82a291da9c292c45973d0d6e3af03603b4c92311aee7cf48187e42-Screenshot_2024-08-23_171410.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. Enter your desired queries or use the provided examples, such as:
   1. [Transactions](/reference/get-all-transactions)
   2. [Blocks](/reference/get-blocks)
   3. [Subscribe](/reference/subscribe-1)
