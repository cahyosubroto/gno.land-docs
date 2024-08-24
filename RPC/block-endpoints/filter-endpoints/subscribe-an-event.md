---
title: "Subscribe an Event"
slug: "subscribe-an-event"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:21:56 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 09:44:02 GMT+0000 (Coordinated Universal Time)"
---
The `subscribe` endpoint starts a subscription to a specific event. This endpoint is particularly useful for monitoring blockchain events as they happen.

> 📘 Note:
> 
> This method is only available for WS connections.

## Available Events

- **newHeads**: Triggers a notification each time a new block header is added to the blockchain. The event data is a Base64-encoded, Amino-encoded binary block header.

## Example Request

In the request example, we need to specify the event that we want to subscribe in the `params` field.

```graphql
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "subscribe",
  "params": [
    "newHeads"
  ]
}
```

## Example Response

```json
{
  "result": "b8934e81-5758-4249-8953-da90aa777ef9",
  "jsonrpc": "2.0",
  "id": 1
}

```

If a `newHeads` event happens, the request will return the following response:

```json
{
  "params": {
    "result": "CscCCgt2MS4wLjAtcmMuMBIFdGVzdDMYyNoZIgsIld2BrQYQouHxZjDgH0JICiALMxWpa/sfrgj51bcYbSgeqSOz0taKXLKCYPIMlE/xjBIkCAISIBIVcZZiQcME2mT2GnLIhbmGWrixQpiH+cGaI9Iqo6ggSiDj49aFmYNf78eBsV6deyeeebleL38O8Ov8/XSgbCalxVog92nrytGOQMQp15Sdl3MG3GaeGdyRMAnaA1rGBVil/QhiIPdp68rRjkDEKdeUnZdzBtxmnhnckTAJ2gNaxgVYpf0IaiC4qGdcWYZSTGBBIl/XuiBtgs1cOjdQQ/BC/N12jhWS7HIggbuwi7zCzwlQP7PCb9EXN2EG7738FHbXIgYPWxBlakiCAShnMXd5cmU0Z3I3bjgyZXpmcGRoZzNueHlwank5Y2FnOXFwa3U1eDZtGpYCCkgKIAszFalr+x+uCPnVtxhtKB6pI7PS1opcsoJg8gyUT/GMEiQIAhIgEhVxlmJBwwTaZPYacsiFuYZauLFCmIf5wZoj0iqjqCASyQEIAhDG2hkiSAogCzMVqWv7H64I+dW3GG0oHqkjs9LWilyygmDyDJRP8YwSJAgCEiASFXGWYkHDBNpk9hpyyIW5hlq4sUKYh/nBmiPSKqOoICoLCJXdga0GEKLh8WYyKGcxd3lyZTRncjduODJlemZwZGhnM254eXBqeTljYWc5cXBrdTV4Nm1CQH5b0jjU1gW8mC+zuCyIPy5xjrfRMSNEvFcHoOjXzc4aEgcW5cYXamXv0WLw2g5RFim2qmgjHnuQorU1YXnWDgw=",
    "subscription": "b8934e81-5758-4249-8953-da90aa777ef9"
  },
  "jsonrpc": "2.0",
  "method": "subscription"
}

```

<br />

## Arguments

### Request Arguments

| **Argument** | **Type**  | **Description**                                                          |
| ------------ | --------- | ------------------------------------------------------------------------ |
| `id`         | `Integer` | The ID of the request, used to match requests and responses in JSON-RPC. |
| `jsonrpc`    | `String`  | Specifies the JSON-RPC protocol version, typically `"2.0"`.              |
| `method`     | `String`  | The method name used for the endpoint.                                   |
| `params`     | `Array`   | An array containing the method's parameters.                             |

### Response Arguments

| **Argument** | **Type**  | **Description**                                                  |
| ------------ | --------- | ---------------------------------------------------------------- |
| `result`     | `Boolean` | The subscription ID, a unique identifier for the subscription.   |
| `jsonrpc`    | `String`  | The JSON-RPC protocol version, `"2.0"`.                          |
| `id`         | `Integer` | The ID of the response, matching the request ID for correlation. |

### Event Response Arguments

| **Argument**   | **Type** | **Description**                                                                |
| -------------- | -------- | ------------------------------------------------------------------------------ |
| `result`       | `String` | The event data, such as the Base64-encoded, Amino-encoded binary block header. |
| `subscription` | `String` | The subscription ID, matching the initial response to correlate the event.     |
| `jsonrpc`      | `String` | The JSON-RPC protocol version, `"2.0"`.                                        |
| `method`       | `String` | The method name, `"subscription"`, indicating an event has occurred.           |
