
# Paystub Deduction

## Structure

`PaystubDeduction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string \| null` | Required | The description of the deduction, as provided on the paystub. For example: `"401(k)"`, `"FICA MED TAX"`. |
| `isPretax` | `boolean \| null` | Required | `true` if the deduction is pre-tax; `false` otherwise. |
| `total` | `number \| null` | Required | The amount of the deduction. |

## Example (as JSON)

```json
{
  "type": "type2",
  "is_pretax": false,
  "total": 221.52
}
```

