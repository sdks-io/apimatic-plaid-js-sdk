
# Student Repayment Plan

An object representing the repayment plan for the student loan

## Structure

`StudentRepaymentPlan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| null` | Required | The description of the repayment plan as provided by the servicer. |
| `type` | [`Type3Enum`](../../doc/models/type-3-enum.md) | Required | The type of the repayment plan. |

## Example (as JSON)

```json
{
  "description": "description8",
  "type": "graduated"
}
```

