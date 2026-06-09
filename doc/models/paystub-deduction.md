
# Paystub Deduction

*This model accepts additional fields of type unknown.*

## Structure

`PaystubDeduction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string \| null` | Required | The description of the deduction, as provided on the paystub. For example: `"401(k)"`, `"FICA MED TAX"`. |
| `isPretax` | `boolean \| null` | Required | `true` if the deduction is pre-tax; `false` otherwise. |
| `total` | `number \| null` | Required | The amount of the deduction. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "type": "type2",
  "is_pretax": false,
  "total": 221.52,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

