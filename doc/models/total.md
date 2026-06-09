
# Total

An object representing both the current pay period and year to date amount for a category.

## Structure

`Total`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `canonicalDescription` | [`CanonicalDescriptionEnum \| undefined`](../../doc/models/canonical-description-enum.md) | Optional | Commonly used term to describe the line item. |
| `description` | `string \| null \| undefined` | Optional | Text of the line item as printed on the paystub. |
| `currentPay` | [`Pay \| undefined`](../../doc/models/pay.md) | Optional | An object representing a monetary amount. |
| `ytdPay` | [`Pay \| undefined`](../../doc/models/pay.md) | Optional | An object representing a monetary amount. |

## Example (as JSON)

```json
{
  "canonical_description": "SOCIAL SECURITY EMPLOYEE TAX",
  "description": "description0",
  "current_pay": {
    "amount": 45.16,
    "currency": "currency4"
  },
  "ytd_pay": {
    "amount": 28.98,
    "currency": "currency0"
  }
}
```

