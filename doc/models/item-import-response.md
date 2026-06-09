
# Item Import Response

ItemImportResponse defines the response schema for `/item/import`

## Structure

`ItemImportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "access_token": "access_token2",
  "request_id": "request_id4"
}
```

