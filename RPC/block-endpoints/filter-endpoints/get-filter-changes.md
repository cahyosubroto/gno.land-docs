---
title: "Get Filter Changes"
slug: "get-filter-changes"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 02:21:24 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Aug 23 2024 09:44:57 GMT+0000 (Coordinated Universal Time)"
---
The `getFilterChanges` endpoint retrieves an array of events since the last time the filter was polled. 

> 📘 Note:
> 
> If a filter is not polled for more than 5 minutes, it is automatically removed to free up resources.

## Example Request

In the request example, we need to specify the filter's ID that we want to retrieve in the `params` field.

```
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "getFilterChanges",
  "params": [
    "c77000bb-700c-41b9-830c-e8b35bdef246"
  ]
}
```

## Example Response

For block filters, the `getFilterChanges` response returns an array of Base64-encoded, Amino-encoded binary block headers.

```
{
  "result": [
    "Cgt2MS4wLjAtcmMuMBIFdGVzdDMYstoZIgsI9teBrQYQ4f+cJzDgH0JICiCOeRC+O7eSKWElYfr3roazF9A23Wvk2AvSWfhU1If41BIkCAISIOmJytoey1P0ZF1/oZUs7Pa7ytV5WJrh41s2PxvWHc4mSiDU0XJ+JFOgK7vm2fVLL29BtwKOGfkv+JxHB1sdgeoSwVog92nrytGOQMQp15Sdl3MG3GaeGdyRMAnaA1rGBVil/QhiIPdp68rRjkDEKdeUnZdzBtxmnhnckTAJ2gNaxgVYpf0IaiC4qGdcWYZSTGBBIl/XuiBtgs1cOjdQQ/BC/N12jhWS7HIggbuwi7zCzwlQP7PCb9EXN2EG7738FHbXIgYPWxBlakiCAShnMXd5cmU0Z3I3bjgyZXpmcGRoZzNueHlwank5Y2FnOXFwa3U1eDZt",
    "Cgt2MS4wLjAtcmMuMBIFdGVzdDMYtNoZIgsIs9iBrQYQ7cjnLDDgH0JICiC9pNnvamowMWsgZczqQ6V5J0YoHNYZWCwFvSFV88+j3xIkCAISIATruI4Rl6mfRoS6GzjaE0aCpWZaYNssV1E+8xRlrDStSiAwCZMWNPsjNM/2fOv37CTjuTPqKW71C5xuBnhEVO5a5Fog92nrytGOQMQp15Sdl3MG3GaeGdyRMAnaA1rGBVil/QhiIPdp68rRjkDEKdeUnZdzBtxmnhnckTAJ2gNaxgVYpf0IaiC4qGdcWYZSTGBBIl/XuiBtgs1cOjdQQ/BC/N12jhWS7HIggbuwi7zCzwlQP7PCb9EXN2EG7738FHbXIgYPWxBlakiCAShnMXd5cmU0Z3I3bjgyZXpmcGRoZzNueHlwank5Y2FnOXFwa3U1eDZt"
  ],
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

| **Argument** | **Type**  | **Description**                                                               |
| ------------ | --------- | ----------------------------------------------------------------------------- |
| `result`     | `String`  | The Base64 encoded, Amino encoded binary data representing the filter result. |
| `jsonrpc`    | `String`  | The JSON-RPC protocol version, `"2.0"`.                                       |
| `id`         | `Integer` | The ID of the response, matching the request ID for correlation.              |
