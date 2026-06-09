
# Bank Transfer Sweep Account

The account where the funds are swept to.

*This model accepts additional fields of type unknown.*

## Structure

`BankTransferSweepAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountNumber` | `string` | Required | - |
| `routingNumber` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_number": "account_number6",
  "routing_number": "routing_number0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

