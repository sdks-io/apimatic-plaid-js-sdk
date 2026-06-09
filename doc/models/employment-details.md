
# Employment Details

An object representing employment details found on a paystub.

*This model accepts additional fields of type unknown.*

## Structure

`EmploymentDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `annualSalary` | [`Pay \| undefined`](../../doc/models/pay.md) | Optional | An object representing a monetary amount. |
| `hireDate` | `string \| null \| undefined` | Optional | Date on which the employee was hired, in the YYYY-MM-DD format. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "annual_salary": {
    "amount": 106.22,
    "currency": "currency0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "hire_date": "2016-03-13T12:52:32.123Z",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

