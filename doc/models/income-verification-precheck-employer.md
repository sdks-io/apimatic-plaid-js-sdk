
# Income Verification Precheck Employer

*This model accepts additional fields of type unknown.*

## Structure

`IncomeVerificationPrecheckEmployer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| null \| undefined` | Optional | The employer's name |
| `taxId` | `string \| null \| undefined` | Optional | The employer's tax id |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "name": "name2",
  "tax_id": "tax_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

