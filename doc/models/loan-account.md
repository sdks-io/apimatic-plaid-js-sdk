
# Loan Account

A loan type account. Supported products for `loan` accounts are: Balance, Liabilities, and Transactions.

## Structure

`LoanAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto` | `string` | Required | Auto loan |
| `business` | `string` | Required | Business loan |
| `commercial` | `string` | Required | Commercial loan |
| `construction` | `string` | Required | Construction loan |
| `consumer` | `string` | Required | Consumer loan |
| `homeEquity` | `string` | Required | Home Equity Line of Credit (HELOC) |
| `loan` | `string` | Required | General loan |
| `mortgage` | `string` | Required | Mortgage loan |
| `overdraft` | `string` | Required | Pre-approved overdraft account, usually tied to a checking account |
| `lineOfCredit` | `string` | Required | Pre-approved line of credit |
| `student` | `string` | Required | Student loan |
| `other` | `string` | Required | Other loan type or unknown loan type |

## Example (as JSON)

```json
{
  "auto": "auto2",
  "business": "business4",
  "commercial": "commercial2",
  "construction": "construction2",
  "consumer": "consumer8",
  "home equity": "home equity4",
  "loan": "loan4",
  "mortgage": "mortgage2",
  "overdraft": "overdraft2",
  "line of credit": "line of credit0",
  "student": "student6",
  "other": "other8"
}
```

