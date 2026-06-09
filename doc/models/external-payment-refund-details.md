
# External Payment Refund Details

## Structure

`ExternalPaymentRefundDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | The name of the account holder. |
| `iban` | `string \| null` | Required | The International Bank Account Number (IBAN) for the account. |
| `bacs` | [`RecipientBACSNullable`](../../doc/models/recipient-bacs-nullable.md) | Required | - |

## Example (as JSON)

```json
{
  "name": "name0",
  "iban": "iban4",
  "bacs": {
    "account": "account4",
    "sort_code": "sort_code4"
  }
}
```

