---
title: "Create a New Block Filter"
slug: "create-a-new-block-filter"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:21:04 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 09:45:17 GMT+0000 (Coordinated Universal Time)"
---
The `newBlockFilter` endpoint creates a filter for the new block events that will notify when a new block arrives.

## Example Request

In the request example, we do not need to specify anything in the `params` field.

```
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "newBlockFilter",
  "params": []
}
```

## Example Response

```
{
  "result": "c77000bb-700c-41b9-830c-e8b35bdef246",
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

| **Argument** | **Type**  | **Description**                                                                         |
| ------------ | --------- | --------------------------------------------------------------------------------------- |
| `result`     | `String`  | The Base64 encoded, Amino encoded binary data representing the new block filter result. |
| `jsonrpc`    | `String`  | The JSON-RPC protocol version, `"2.0"`.                                                 |
| `id`         | `Integer` | The ID of the response, matching the request ID for correlation.                        |
