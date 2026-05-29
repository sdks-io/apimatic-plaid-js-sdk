
# Distribution Details

An object representing information about a distribution from the paycheck (for example, the amount distributed to a specific checking account, or to a retirement plan).

*This model accepts additional fields of type unknown.*

## Structure

`DistributionDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountNumber` | `string \| null \| undefined` | Optional | The account number of the account being deposited to. |
| `bankAccountType` | `string \| null \| undefined` | Optional | The type of bank account (e.g. Checking or Savings) |
| `bankName` | `string \| null \| undefined` | Optional | The name of the bank that the payment is being deposited to. |
| `currentPay` | [`Pay \| undefined`](../../doc/models/pay.md) | Optional | An object representing a monetary amount. |
| `description` | `string \| null \| undefined` | Optional | A description of the distribution type. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_number": "account_number8",
  "bank_account_type": "bank_account_type0",
  "bank_name": "bank_name2",
  "current_pay": {
    "amount": 45.16,
    "currency": "currency4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "description": "description2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

