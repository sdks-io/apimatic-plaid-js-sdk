
# Income Verification Precheck Military Info

## Structure

`IncomeVerificationPrecheckMilitaryInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isActiveDuty` | `boolean \| null \| undefined` | Optional | Is the user currently active duty in the US military |
| `branch` | [`BranchEnum \| undefined`](../../doc/models/branch-enum.md) | Optional | If the user is currently serving in the US military, the branch of the military they are serving in |

## Example (as JSON)

```json
{
  "is_active_duty": false,
  "branch": "NAVY"
}
```

