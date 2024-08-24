---
title: "JSON-RPC API Overview"
slug: "rpc-api"
excerpt: ""
hidden: false
createdAt: "Fri Aug 23 2024 07:41:15 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Sat Aug 24 2024 05:18:50 GMT+0000 (Coordinated Universal Time)"
---
`tx-indexer` also includes a JSON-RPC API server that processes requests and responses according to the [JSON-RPC 2.0 standard](https://www.jsonrpc.org/specification). This API uses positional function parameters, meaning each JSON-RPC request must use arrays, not objects, as the parameter types. We provide the following endpoints which you can use:

- [Block Endpoints](https://gnoland.readme.io/reference/get-block)
- [Transaction Endpoints](https://gnoland.readme.io/reference/get-tx-result)
- [Filter Endpoints](https://gnoland.readme.io/reference/create-a-new-block-filter)

## Access the API

You can use Postman or `curl method` to test and access the RPC API.

### `curl` Method

Use the following template to call the JSON-RPC API using `curl` method:

```Text bash
curl -X POST http://localhost:8546 -H "Content-Type: application/json" \
-d '{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "<method_name>",
  "params": [
    <parameters>
  ]
}'

```

### Postman

1. Download and install [Postman](https://www.postman.com/downloads/).
2. Open **Postman** and click the **New** button to create a new request.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f8b01cdf9788392d836351a7363c29c62e06bcbe9636e6e1ebcda15f3e2e1db0-Group_42_41.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. Select the **HTTP** method.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b7950e1b9ebe0b84d6072eb82717793203b457dd8f45498ede9de9f72db16a8-Group_42_42.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


4. Select **Post** method > enter the URL `http://localhost:8546/`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f94b640a4e5d09d6a800e844127696dee7cee090883d9b9aa2baa0d754426488-Group_42_43.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


5. Select the **Body** tab > **raw**  > **JSON**.
6. Enter the JSON-RPC request. You can get a request example in our documentation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea2219dddd8d05ccf7cdd6ff5989dc5ec7338b0cc33e895fb02995f80f6b1e1c-Group_42_44.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


7. Click the **Send** button and get a response.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3dcc8b01ea993313e888ce795976abf3f8e8b92cbaf014b08ba8b42cef2f7fe-Screenshot_2024-08-23_174956.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]
