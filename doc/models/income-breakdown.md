
# Income Breakdown

An object representing a breakdown of the different income types on the paystub.

## Structure

`IncomeBreakdown`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type5Enum`](../../doc/models/type-5-enum.md) | Required | The type of income. Possible values include:<br>`"regular"`: regular income<br>`"overtime"`: overtime income<br>`"bonus"`: bonus income |
| `rate` | `number \| null` | Required | The hourly rate at which the income is paid. |
| `hours` | `number \| null` | Required | The number of hours logged for this income for this pay period. |
| `total` | `number \| null` | Required | The total pay for this pay period. |

## Example (as JSON)

```json
{
  "type": "regular",
  "rate": 190.0,
  "hours": 102.08,
  "total": 23.2
}
```

