
# Mortgage Interest Rate

Object containing metadata about the interest rate for the mortgage.

## Structure

`MortgageInterestRate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `number \| null` | Required | Percentage value (interest rate of current mortgage, not APR) of interest payable on a loan. |
| `type` | `string \| null` | Required | The type of interest charged (fixed or variable). |

## Example (as JSON)

```json
{
  "percentage": 151.72,
  "type": "type6"
}
```

