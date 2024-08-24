---
title: "Best Practices"
slug: "best-practices"
excerpt: ""
hidden: false
createdAt: "Sat Aug 24 2024 02:28:06 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 05:15:28 GMT+0000 (Coordinated Universal Time)"
---
To get you up to speed with the gno.land `tx-indexer` tool, we’ve compiled some best practices to help you explore its features and APIs.

> 📘 Note:
> 
> These suggestions are based on our developers' experiences, but you should adapt `tx-indexer` to fit the specific needs of your app or project.

## 1. Use the Pre-defined Endpoints

Once you have installed and run the `tx-indexer`, you can access our pre-defined custom endpoints that are suitable for the general use cases at `http://test3.gno.land:36657/` for the starter. You can click on these endpoints and change the request parameters in the URL directly in your browser.

## 2. Get the Correct Testnet Parameters

Access the GraphQL APIs at `http://localhost:8546/graphql` and use our use cases to get the testnet parameters for your use case. You can use these parameters to customize your GraphQL query or use them to call the JSON-RPC APIs.

## 3. Read the GraphQL Documentation

You can use our use case in our documentation, or you can read the GraphQL root and schema-type documentation directly at `http\://localhost:8546/graphql` so you can use a query that suits your project needs.

## 4. Correct URL

To test the JSON-RPC API, make sure to use the correct listed address, which is if you use our testnet `http://test3.gno.land:36657/` by default, the listen address will be `http://localhost:8546`.
