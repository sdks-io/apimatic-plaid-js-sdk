
# Item Public Token Exchange Response

ItemPublicTokenExchangeResponse defines the response schema for `/item/public_token/exchange`

*This model accepts additional fields of type unknown.*

## Structure

`ItemPublicTokenExchangeResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `itemId` | `string` | Required | The `item_id` value of the Item associated with the returned `access_token` |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "access_token": "access_token4",
  "item_id": "item_id6",
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

