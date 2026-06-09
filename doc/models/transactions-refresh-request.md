
# Transactions Refresh Request

TransactionsRefreshRequest defines the request schema for `/transactions/refresh`

## Structure

`TransactionsRefreshRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "access_token": "access_token6",
  "secret": "secret6"
}
```

