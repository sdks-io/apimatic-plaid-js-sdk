
# Liabilities Get Request

LiabilitiesGetRequest defines the request schema for `/liabilities/get`

## Structure

`LiabilitiesGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `options` | [`LiabilitiesGetRequestOptions \| undefined`](../../doc/models/liabilities-get-request-options.md) | Optional | An optional object to filter `/liabilities/get` results. If provided, `options` cannot be null. |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "secret": "secret6",
  "access_token": "access_token6",
  "options": {
    "account_ids": [
      "account_ids3",
      "account_ids4",
      "account_ids5"
    ]
  }
}
```

