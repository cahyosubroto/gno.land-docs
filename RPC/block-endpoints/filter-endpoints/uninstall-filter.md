---
title: "Uninstall Filter"
slug: "uninstall-filter"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:21:41 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 09:44:20 GMT+0000 (Coordinated Universal Time)"
---
The `uninstallFilter` endpoint uninstalls a filter.

## Example Request

In the request example, we need to specify the filter's ID that we want to uninstall in the `params` field.

```
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "uninstallFilter",
  "params": [
    "c77000bb-700c-41b9-830c-e8b35bdef246"
  ]
}
```

## Example Response

```
{
  "result": true,
  "jsonrpc": "2.0",
  "id": 1
}
```

## Arguments

### Request Arguments

| **Argument** | **Type**  | **Description**                                                          |
| ------------ | --------- | ------------------------------------------------------------------------ |
| `id`         | `Integer` | The ID of the request, used to match requests and responses in JSON-RPC. |
| `jsonrpc`    | `String`  | Specifies the JSON-RPC protocol version, typically `"2.0"`.              |
| `method`     | `String`  | The method name used for the endpoint.                                   |
| `params`     | `Array`   | An array containing the method's parameters.                             |

### Response Arguments

| **Argument** | **Type**  | **Description**                                                                      |
| ------------ | --------- | ------------------------------------------------------------------------------------ |
| `result`     | `Boolean` | Indicates whether the filter was successfully uninstalled (`true`) or not (`false`). |
| `jsonrpc`    | `String`  | The JSON-RPC protocol version, `"2.0"`.                                              |
| `id`         | `Integer` | The ID of the response, matching the request ID for correlation.                     |
