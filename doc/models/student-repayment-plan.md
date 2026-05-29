
# Student Repayment Plan

An object representing the repayment plan for the student loan

*This model accepts additional fields of type unknown.*

## Structure

`StudentRepaymentPlan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| null` | Required | The description of the repayment plan as provided by the servicer. |
| `type` | [`Type3`](../../doc/models/type-3.md) | Required | The type of the repayment plan. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "description": "description8",
  "type": "graduated",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

