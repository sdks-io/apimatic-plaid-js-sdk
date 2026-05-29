
# Mortgage Liability

Contains details about a mortgage account.

*This model accepts additional fields of type unknown.*

## Structure

`MortgageLiability`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The ID of the account that this liability belongs to. |
| `accountNumber` | `string` | Required | The account number of the loan. |
| `currentLateFee` | `number \| null` | Required | The current outstanding amount charged for late payment. |
| `escrowBalance` | `number \| null` | Required | Total amount held in escrow to pay taxes and insurance on behalf of the borrower. |
| `hasPmi` | `boolean \| null` | Required | Indicates whether the borrower has private mortgage insurance in effect. |
| `hasPrepaymentPenalty` | `boolean \| null` | Required | Indicates whether the borrower will pay a penalty for early payoff of mortgage. |
| `interestRate` | [`MortgageInterestRate`](../../doc/models/mortgage-interest-rate.md) | Required | Object containing metadata about the interest rate for the mortgage. |
| `lastPaymentAmount` | `number \| null` | Required | The amount of the last payment. |
| `lastPaymentDate` | `string \| null` | Required | The date of the last payment. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `loanTypeDescription` | `string \| null` | Required | Description of the type of loan, for example `conventional`, `fixed`, or `variable`. This field is provided directly from the loan servicer and does not have an enumerated set of possible values. |
| `loanTerm` | `string \| null` | Required | Full duration of mortgage as at origination (e.g. `10 year`). |
| `maturityDate` | `string \| null` | Required | Original date on which mortgage is due in full. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `nextMonthlyPayment` | `number \| null` | Required | The amount of the next payment. |
| `nextPaymentDueDate` | `string \| null` | Required | The due date for the next payment. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `originationDate` | `string \| null` | Required | The date on which the loan was initially lent. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `originationPrincipalAmount` | `number \| null` | Required | The original principal balance of the mortgage. |
| `pastDueAmount` | `number \| null` | Required | Amount of loan (principal + interest) past due for payment. |
| `propertyAddress` | [`MortgagePropertyAddress`](../../doc/models/mortgage-property-address.md) | Required | Object containing fields describing property address. |
| `ytdInterestPaid` | `number \| null` | Required | The year to date (YTD) interest paid. |
| `ytdPrincipalPaid` | `number \| null` | Required | The YTD principal paid. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_id": "account_id6",
  "account_number": "account_number4",
  "current_late_fee": 37.04,
  "escrow_balance": 38.4,
  "has_pmi": false,
  "has_prepayment_penalty": false,
  "interest_rate": {
    "percentage": 105.9,
    "type": "type2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "last_payment_amount": 42.16,
  "last_payment_date": "2016-03-13T12:52:32.123Z",
  "loan_type_description": "loan_type_description8",
  "loan_term": "loan_term0",
  "maturity_date": "2016-03-13T12:52:32.123Z",
  "next_monthly_payment": 31.64,
  "next_payment_due_date": "2016-03-13T12:52:32.123Z",
  "origination_date": "2016-03-13T12:52:32.123Z",
  "origination_principal_amount": 68.32,
  "past_due_amount": 170.88,
  "property_address": {
    "city": "city0",
    "country": "country4",
    "postal_code": "postal_code2",
    "region": "region6",
    "street": "street0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "ytd_interest_paid": 179.02,
  "ytd_principal_paid": 212.0,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

