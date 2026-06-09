
# Signal Decision Report Request

SignalDecisionReportRequest defines the request schema for `/signal/decision/report`

## Structure

`SignalDecisionReportRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `clientTransactionId` | `string` | Required | Must be the same as the `client_transaction_id` supplied when calling `/signal/evaluate` |
| `initiated` | `boolean` | Required | `true` if the ACH transaction was initiated, `false` otherwise. |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "client_transaction_id": "client_transaction_id2",
  "initiated": false
}
```

