
# Sandbox Item Reset Login Request

SandboxItemResetLoginRequest defines the request schema for `/sandbox/item/reset_login`

## Structure

`SandboxItemResetLoginRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret8",
  "access_token": "access_token0"
}
```

