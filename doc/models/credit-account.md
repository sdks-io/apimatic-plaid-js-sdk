
# Credit Account

A credit card type account. Supported products for `credit` accounts are: Balance, Transactions, Identity, and Liabilities.

*This model accepts additional fields of type unknown.*

## Structure

`CreditAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `creditCard` | `string` | Required | Bank-issued credit card |
| `paypal` | `string` | Required | PayPal-issued credit card |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "credit card": "credit card2",
  "paypal": "paypal4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

