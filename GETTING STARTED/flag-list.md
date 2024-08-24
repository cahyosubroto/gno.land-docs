---
title: "Flag List"
slug: "flag-list"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 05:54:34 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 05:55:01 GMT+0000 (Coordinated Universal Time)"
---
You can see the full list of the available flags by running the following commands:

```powershell
./build/tx-indexer start --help
```

| Flag                        | Description                                                | Default Value            |
| --------------------------- | ---------------------------------------------------------- | ------------------------ |
| `-db-path indexer-db`       | The absolute path for the indexer DB (embedded).           | `indexer-db`             |
| `-http-rate-limit <number>` | The maximum HTTP requests allowed per minute per IP.       | `0` (unlimited)          |
| `-listen-address <URL>`     | The `IP:PORT` URL for the indexer JSON-RPC server.         | `0.0.0.0:8546`           |
| `-log-level <log_type>`     | The log level for the CLI output.                          | `info`                   |
| `-max-chunk-size <number>`  | The range for fetching blockchain data by a single worker. | `100`                    |
| `-max-slots <number>`       | The number of slots (workers) the fetcher employs.         | `100`                    |
| `-remote <URL>`             | The JSON-RPC URL of the Gno chain.                         | `http://127.0.0.1:26657` |
