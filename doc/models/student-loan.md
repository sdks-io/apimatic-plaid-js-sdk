
# Student Loan

Contains details about a student loan account

## Structure

`StudentLoan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string \| null` | Required | The ID of the account that this liability belongs to. |
| `accountNumber` | `string \| null` | Required | The account number of the loan. For some institutions, this may be a masked version of the number (e.g., the last 4 digits instead of the entire number). |
| `disbursementDates` | `string[] \| null` | Required | The dates on which loaned funds were disbursed or will be disbursed. These are often in the past. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `expectedPayoffDate` | `string \| null` | Required | The date when the student loan is expected to be paid off. Availability for this field is limited. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `guarantor` | `string \| null` | Required | The guarantor of the student loan. |
| `interestRatePercentage` | `number` | Required | The interest rate on the loan as a percentage. |
| `isOverdue` | `boolean \| null` | Required | `true` if a payment is currently overdue. Availability for this field is limited. |
| `lastPaymentAmount` | `number \| null` | Required | The amount of the last payment. |
| `lastPaymentDate` | `string \| null` | Required | The date of the last payment. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `lastStatementIssueDate` | `string \| null` | Required | The date of the last statement. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `loanName` | `string \| null` | Required | The type of loan, e.g., "Consolidation Loans". |
| `loanStatus` | [`StudentLoanStatus`](../../doc/models/student-loan-status.md) | Required | An object representing the status of the student loan |
| `minimumPaymentAmount` | `number \| null` | Required | The minimum payment due for the next billing cycle. There are some exceptions:<br>Some institutions require a minimum payment across all loans associated with an account number. Our API presents that same minimum payment amount on each loan. The institutions that do this are: Great Lakes ( `ins_116861`), Firstmark (`ins_116295`), Commonbond Firstmark Services (`ins_116950`), Nelnet (`ins_116528`), EdFinancial Services (`ins_116304`), Granite State (`ins_116308`), and Oklahoma Student Loan Authority (`ins_116945`).<br>Firstmark (`ins_116295` ) will display as $0 if there is an autopay program in effect. |
| `nextPaymentDueDate` | `string \| null` | Required | The due date for the next payment. The due date is `null` if a payment is not expected. A payment is not expected if `loan_status.type` is `deferment`, `in_school`, `consolidated`, `paid in full`, or `transferred`. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `originationDate` | `string \| null` | Required | The date on which the loan was initially lent. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `originationPrincipalAmount` | `number \| null` | Required | The original principal balance of the loan. |
| `outstandingInterestAmount` | `number \| null` | Required | The total dollar amount of the accrued interest balance. For Sallie Mae ( `ins_116944`), this amount is included in the current balance of the loan, so this field will return as `null`. |
| `paymentReferenceNumber` | `string \| null` | Required | The relevant account number that should be used to reference this loan for payments. In the majority of cases, `payment_reference_number` will match a`ccount_number,` but in some institutions, such as Great Lakes (`ins_116861`), it will be different. |
| `pslfStatus` | [`PSLFStatus`](../../doc/models/pslf-status.md) | Required | Information about the student's eligibility in the Public Service Loan Forgiveness program. This is only returned if the institution is Fedloan (`ins_116527`). |
| `repaymentPlan` | [`StudentRepaymentPlan`](../../doc/models/student-repayment-plan.md) | Required | An object representing the repayment plan for the student loan |
| `sequenceNumber` | `string \| null` | Required | The sequence number of the student loan. Heartland ECSI (`ins_116948`) does not make this field available. |
| `servicerAddress` | [`ServicerAddressData`](../../doc/models/servicer-address-data.md) | Required | The address of the student loan servicer. This is generally the remittance address to which payments should be sent. |
| `ytdInterestPaid` | `number \| null` | Required | The year to date (YTD) interest paid. Availability for this field is limited. |
| `ytdPrincipalPaid` | `number \| null` | Required | The year to date (YTD) principal paid. Availability for this field is limited. |

## Example (as JSON)

```json
{
  "account_id": "account_id0",
  "account_number": "account_number8",
  "disbursement_dates": [
    "2016-03-13T12:52:32.123Z",
    "2016-03-13T12:52:32.123Z"
  ],
  "expected_payoff_date": "2016-03-13T12:52:32.123Z",
  "guarantor": "guarantor8",
  "interest_rate_percentage": 51.16,
  "is_overdue": false,
  "last_payment_amount": 84.52,
  "last_payment_date": "2016-03-13T12:52:32.123Z",
  "last_statement_issue_date": "2016-03-13T12:52:32.123Z",
  "loan_name": "loan_name4",
  "loan_status": {
    "end_date": "2016-03-13T12:52:32.123Z",
    "type": "cancelled"
  },
  "minimum_payment_amount": 153.02,
  "next_payment_due_date": "2016-03-13T12:52:32.123Z",
  "origination_date": "2016-03-13T12:52:32.123Z",
  "origination_principal_amount": 25.96,
  "outstanding_interest_amount": 143.24,
  "payment_reference_number": "payment_reference_number8",
  "pslf_status": {
    "estimated_eligibility_date": "2016-03-13T12:52:32.123Z",
    "payments_made": 175.34,
    "payments_remaining": 221.32
  },
  "repayment_plan": {
    "description": "description6",
    "type": "income-based repayment"
  },
  "sequence_number": "sequence_number8",
  "servicer_address": {
    "city": "city2",
    "region": "region8",
    "street": "street2",
    "postal_code": "postal_code4",
    "country": "country6"
  },
  "ytd_interest_paid": 136.66,
  "ytd_principal_paid": 86.36
}
```

