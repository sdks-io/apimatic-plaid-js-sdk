
# W2 State and Local Wages

## Structure

`W2StateAndLocalWages`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | `string \| null \| undefined` | Optional | State associated with the wage. |
| `employerStateIdNumber` | `string \| null \| undefined` | Optional | State identification number of the employer. |
| `stateWagesTips` | `string \| null \| undefined` | Optional | Wages and tips from the specified state. |
| `stateIncomeTax` | `string \| null \| undefined` | Optional | Income tax from the specified state. |
| `localWagesTips` | `string \| null \| undefined` | Optional | Wages and tips from the locality. |
| `localIncomeTax` | `string \| null \| undefined` | Optional | Income tax from the locality. |
| `localityName` | `string \| null \| undefined` | Optional | Name of the locality. |

## Example (as JSON)

```json
{
  "state": "state8",
  "employer_state_id_number": "employer_state_id_number4",
  "state_wages_tips": "state_wages_tips4",
  "state_income_tax": "state_income_tax0",
  "local_wages_tips": "local_wages_tips4"
}
```

