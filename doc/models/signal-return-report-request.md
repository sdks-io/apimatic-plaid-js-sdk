
# Signal Return Report Request

SignalReturnReportRequest defines the request schema for `/signal/return/report`

## Structure

`SignalReturnReportRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `clientTransactionId` | `string` | Required | Must be the same as the `client_transaction_id` supplied when calling `/signal/evaluate` |
| `returnCode` | `string` | Required | Must be a valid ACH return code (e.g. "R01") |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret8",
  "client_transaction_id": "client_transaction_id6",
  "return_code": "return_code6"
}
```

