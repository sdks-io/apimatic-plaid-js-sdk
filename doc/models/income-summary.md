
# Income Summary

The verified fields from a paystub verification. All fields are provided as reported on the paystub.

## Structure

`IncomeSummary`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `employerName` | [`EmployerIncomeSummaryFieldString`](../../doc/models/employer-income-summary-field-string.md) | Required | - |
| `employeeName` | [`EmployeeIncomeSummaryFieldString`](../../doc/models/employee-income-summary-field-string.md) | Required | - |
| `ytdGrossIncome` | [`YTDGrossIncomeSummaryFieldNumber`](../../doc/models/ytd-gross-income-summary-field-number.md) | Required | - |
| `ytdNetIncome` | [`YTDNetIncomeSummaryFieldNumber`](../../doc/models/ytd-net-income-summary-field-number.md) | Required | - |
| `payFrequency` | [`PayFrequency`](../../doc/models/pay-frequency.md) | Required | - |
| `projectedWage` | [`ProjectedIncomeSummaryFieldNumber`](../../doc/models/projected-income-summary-field-number.md) | Required | - |
| `verifiedTransaction` | [`TransactionData`](../../doc/models/transaction-data.md) | Required | Information about the matched direct deposit transaction used to verify a user's payroll information. |

## Example (as JSON)

```json
{
  "employer_name": {
    "value": "value8",
    "verification_status": "UNKNOWN"
  },
  "employee_name": {
    "value": "value4",
    "verification_status": "UNABLE_TO_VERIFY"
  },
  "ytd_gross_income": {
    "value": 80.36,
    "verification_status": "UNKNOWN"
  },
  "ytd_net_income": {
    "value": 101.8,
    "verification_status": "UNABLE_TO_VERIFY"
  },
  "pay_frequency": {
    "value": "monthly",
    "verification_status": "UNABLE_TO_VERIFY"
  },
  "projected_wage": {
    "value": 108.54,
    "verification_status": "NEEDS_INFO"
  },
  "verified_transaction": {
    "description": "description8",
    "amount": 228.3,
    "date": "2016-03-13T12:52:32.123Z",
    "account_id": "account_id0",
    "transaction_id": "transaction_id6"
  }
}
```

