
# Processor Stripe Bank Account Token Create Response

ProcessorStripeBankAccountTokenCreateResponse defines the response schema for `/processor/stripe/bank_account/create`

## Structure

`ProcessorStripeBankAccountTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stripeBankAccountToken` | `string` | Required | A token that can be sent to Stripe for use in making API calls to Plaid |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "stripe_bank_account_token": "stripe_bank_account_token0",
  "request_id": "request_id6"
}
```

