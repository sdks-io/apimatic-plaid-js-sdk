
# Bank Transfer Balance Get Response

Defines the response schema for `/bank_transfer/balance/get`

*This model accepts additional fields of type unknown.*

## Structure

`BankTransferBalanceGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `balance` | [`BankTransferBalance`](../../doc/models/bank-transfer-balance.md) | Required | - |
| `originationAccountId` | `string \| null` | Required | The ID of the origination account that this balance belongs to. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "balance": {
    "available": "available8",
    "transactable": "transactable6",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "origination_account_id": "origination_account_id6",
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

