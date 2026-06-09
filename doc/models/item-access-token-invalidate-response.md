
# Item Access Token Invalidate Response

ItemAccessTokenInvalidateResponse defines the response schema for `/item/access_token/invalidate`

## Structure

`ItemAccessTokenInvalidateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `newAccessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "new_access_token": "new_access_token4",
  "request_id": "request_id0"
}
```

