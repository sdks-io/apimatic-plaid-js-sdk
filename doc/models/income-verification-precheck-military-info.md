
# Income Verification Precheck Military Info

*This model accepts additional fields of type unknown.*

## Structure

`IncomeVerificationPrecheckMilitaryInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isActiveDuty` | `boolean \| null \| undefined` | Optional | Is the user currently active duty in the US military |
| `branch` | [`Branch \| undefined`](../../doc/models/branch.md) | Optional | If the user is currently serving in the US military, the branch of the military they are serving in |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "is_active_duty": false,
  "branch": "NAVY",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

