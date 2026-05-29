
# Bank Transfer Cancel Request

Defines the request schema for `/bank_transfer/cancel`

*This model accepts additional fields of type unknown.*

## Structure

`BankTransferCancelRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `bankTransferId` | `string` | Required | Plaid’s unique identifier for a bank transfer. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret8",
  "bank_transfer_id": "bank_transfer_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

