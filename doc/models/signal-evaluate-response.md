
# Signal Evaluate Response

SignalEvaluateResponse defines the response schema for `/signal/income/evaluate`

## Structure

`SignalEvaluateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `scores` | [`SignalEvaluateScores`](../../doc/models/signal-evaluate-scores.md) | Required | Risk scoring details broken down by risk category. |
| `coreAttributes` | [`SignalEvaluateCoreAttributes`](../../doc/models/signal-evaluate-core-attributes.md) | Required | The core attributes object contains additional data that can be used to assess the ACH return risk, such as past ACH return events, balance/transaction history, the Item’s connection history in the Plaid network, and identity change history. |

## Example (as JSON)

```json
{
  "request_id": "request_id2",
  "scores": {
    "customer_initiated_return_risk": {
      "score": 100,
      "risk_tier": 5
    },
    "bank_initiated_return_risk": {
      "score": 100,
      "risk_tier": 8
    }
  },
  "core_attributes": {
    "unauthorized_transactions_count_7d": 240,
    "unauthorized_transactions_count_30d": 124,
    "unauthorized_transactions_count_60d": 208,
    "unauthorized_transactions_count_90d": 164,
    "nsf_overdraft_transactions_count_7d": 44
  }
}
```

