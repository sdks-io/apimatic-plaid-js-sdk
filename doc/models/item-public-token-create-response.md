
# Item Public Token Create Response

ItemPublicTokenCreateResponse defines the response schema for `/item/public_token/create`

## Structure

`ItemPublicTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `publicToken` | `string` | Required | A `public_token` for the particular Item corresponding to the specified `access_token` |
| `expiration` | `string \| undefined` | Optional | - |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "public_token": "public_token4",
  "expiration": "2016-03-13T12:52:32.123Z",
  "request_id": "request_id6"
}
```

