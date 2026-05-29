
# Mortgage Interest Rate

Object containing metadata about the interest rate for the mortgage.

*This model accepts additional fields of type unknown.*

## Structure

`MortgageInterestRate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `number \| null` | Required | Percentage value (interest rate of current mortgage, not APR) of interest payable on a loan. |
| `type` | `string \| null` | Required | The type of interest charged (fixed or variable). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "percentage": 151.72,
  "type": "type6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

