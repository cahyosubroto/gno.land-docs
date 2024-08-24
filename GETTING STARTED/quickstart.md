---
title: "Quickstart"
slug: "quickstart"
excerpt: ""
hidden: false
createdAt: "Thu Aug 22 2024 09:15:51 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 05:13:58 GMT+0000 (Coordinated Universal Time)"
---
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c61217e8dbe007a93405a2ae68a7cd026b991b37cb66f1dec65de0fbc936ca4-Asset_1300x_16.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


Follow the steps below to get started with the `tx-indexer`.

## 1. Install `tx-indexer`

To begin using `tx-indexer`, you must install it locally. Follow the steps [here](https://gnoland.readme.io/reference/installation) to install and run the `tx-indexer`.

## 2. Access and Test the GraphQL Endpoints

We provide [GraphQL endpoints](/reference/-graphql-api) that support standard queries for transactions and blocks. You can access a GraphQL playground at `http://localhost:8546/graphql`.

## 3. Test the RPC Endpoints in Postman

We also provide [JSON-RPC Endpoints](/reference/rpc-api) that adhere to the **JSON-RPC 2.0 standard**. You can use `curl` method, or you can test it using Postman.

> 📘 Note:
> 
> We recommend using a library that supports **JSON RPC 2.0** clients to integrate with your services.

Now that you have played around with the API, you can use it to retrieve and manage the transaction and block data generated on the Tendermint network.
