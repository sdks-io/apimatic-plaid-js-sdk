
# Transactions Get Request

TransactionsGetRequest defines the request schema for `/transactions/get`

## Structure

`TransactionsGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `options` | [`TransactionsGetRequestOptions \| undefined`](../../doc/models/transactions-get-request-options.md) | Optional | An optional object to be used with the request. If specified, `options` must not be `null`. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `startDate` | `string` | Required | The earliest date for which data should be returned. Dates should be formatted as YYYY-MM-DD. |
| `endDate` | `string` | Required | The latest date for which data should be returned. Dates should be formatted as YYYY-MM-DD. |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "options": {
    "account_ids": [
      "account_ids3",
      "account_ids4",
      "account_ids5"
    ],
    "count": 98,
    "offset": 50,
    "include_original_description": false,
    "include_personal_finance_category_beta": false
  },
  "access_token": "access_token8",
  "secret": "secret6",
  "start_date": "2016-03-13T12:52:32.123Z",
  "end_date": "2016-03-13T12:52:32.123Z"
}
```

