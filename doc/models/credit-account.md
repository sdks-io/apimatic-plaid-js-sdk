
# Credit Account

A credit card type account. Supported products for `credit` accounts are: Balance, Transactions, Identity, and Liabilities.

## Structure

`CreditAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `creditCard` | `string` | Required | Bank-issued credit card |
| `paypal` | `string` | Required | PayPal-issued credit card |

## Example (as JSON)

```json
{
  "credit card": "credit card2",
  "paypal": "paypal4"
}
```

