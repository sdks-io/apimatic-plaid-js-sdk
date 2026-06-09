
# Credit Card Liability

An object representing a credit card account.

## Structure

`CreditCardLiability`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string \| null` | Required | The ID of the account that this liability belongs to. |
| `aprs` | [`APR[]`](../../doc/models/apr.md) | Required | The various interest rates that apply to the account. |
| `isOverdue` | `boolean \| null` | Required | true if a payment is currently overdue. Availability for this field is limited. |
| `lastPaymentAmount` | `number` | Required | The amount of the last payment. |
| `lastPaymentDate` | `string` | Required | The date of the last payment. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). Availability for this field is limited. |
| `lastStatementIssueDate` | `string` | Required | The date of the last statement. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `minimumPaymentAmount` | `number` | Required | The minimum payment due for the next billing cycle. |
| `nextPaymentDueDate` | `string \| null` | Required | The due date for the next payment. The due date is `null` if a payment is not expected. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |

## Example (as JSON)

```json
{
  "account_id": "account_id4",
  "aprs": [
    {
      "apr_percentage": 185.0,
      "apr_type": "balance_transfer_apr",
      "balance_subject_to_apr": 23.44,
      "interest_charge_amount": 112.32
    }
  ],
  "is_overdue": false,
  "last_payment_amount": 189.28,
  "last_payment_date": "2016-03-13T12:52:32.123Z",
  "last_statement_issue_date": "2016-03-13T12:52:32.123Z",
  "minimum_payment_amount": 48.26,
  "next_payment_due_date": "2016-03-13T12:52:32.123Z"
}
```

