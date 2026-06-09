
# Student Loan Repayment Model

Student loan repayment information used to configure Sandbox test data for the Liabilities product

*This model accepts additional fields of type unknown.*

## Structure

`StudentLoanRepaymentModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string` | Required | The only currently supported value for this field is `standard`. |
| `nonRepaymentMonths` | `number` | Required | Configures the number of months before repayment starts. |
| `repaymentMonths` | `number` | Required | Configures the number of months of repayments before the loan is paid off. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "type": "type4",
  "non_repayment_months": 95.52,
  "repayment_months": 162.18,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

