---
title: "Unsubscribe an Event"
slug: "unsubscribe-an-event"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:22:05 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 09:43:37 GMT+0000 (Coordinated Universal Time)"
---
The `unsubscribe` endpoint cancels an existing subscription, stopping further events from being sent to the client. 

> 📘 Note:
> 
> This method is only available for WS connections.

## Example Request

In the request example, we need to specify the subscription ID that we want to cancel in the `params` field.

```graphql
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "unsubscribe",
  "params": [
    "b8934e81-5758-4249-8953-da90aa777ef9"
  ]
}
```

## Example Response

```json
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

| **Argument** | **Type**  | **Description**                                                                         |
| ------------ | --------- | --------------------------------------------------------------------------------------- |
| `result`     | `Boolean` | Indicates whether the subscription was successfully canceled (`true`) or not (`false`). |
| `jsonrpc`    | `String`  | The JSON-RPC protocol version, `"2.0"`.                                                 |
| `id`         | `Integer` | The ID of the response, matching the request ID for correlation.                        |
