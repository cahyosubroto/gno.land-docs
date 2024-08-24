---
title: "Installation"
slug: "installation"
excerpt: ""
hidden: false
createdAt: "Thu Aug 22 2024 07:50:24 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 02:29:08 GMT+0000 (Coordinated Universal Time)"
---
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35ddcbd40ccb4fe306d48d1ce1721933b1f234f9addad8c075de1c6b576f2603-Asset_2300x_14.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


This guide will show you how to install and run the `tx-indexer`  by using the `<http://test3.gno.land:36657>` URL, which we offer as a testnet for you to experiment with.

## Prerequisites

- [Go](https://golang.org/dl/) v1.18 or later.
- [GNU Make](https://www.gnu.org/software/make/) v3.81 or later.

## 1. Clone the GitHub Repository

Clone the GitHub repository using the following command:

```powershell
git clone https://github.com/gnolang/tx-indexer.git
```

## 2. Run `tx-indexer`

1. Build the `tx-indexer` binary using either of the commands:

```powershell
# Using Go
go build -o build/tx-indexer ./cmd

# Using make
make build
```

2. Run the `tx-indexer` using the following command to access the API at `http://localhost:8546`:

> 📘 Note:
> 
> For the full list of the available flag that you can use, please see [here](https://gnoland.readme.io/reference/flag-list).

```powershell
./build/tx-indexer start --remote http://test3.gno.land:36657 --db-path indexer-db

or

go run cmd/main.go cmd/start.go cmd/waiter.go start --remote http://test3.gno.land:36657 --db-path indexer-db
```

Once you have installed and run the `tx-indexer` play around with the [JSON-RPC API](/reference/rpc-api) or [GraphQL API](/reference/graphql-api) API on how to retrieve the data from the blockchain.

> 📘 Note:
> 
> `tx-indexer` also provides websocket endpoint at `ws://<listen-address>/ws`.
