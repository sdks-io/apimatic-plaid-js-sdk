
# Account Filters Response

The `account_filters` specified in the original call to `/link/token/create`.

## Structure

`AccountFiltersResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depository` | [`DepositoryFilter \| undefined`](../../doc/models/depository-filter.md) | Optional | A filter to apply to `depository`-type accounts |
| `credit` | [`CreditFilter \| undefined`](../../doc/models/credit-filter.md) | Optional | A filter to apply to `credit`-type accounts |
| `loan` | [`LoanFilter \| undefined`](../../doc/models/loan-filter.md) | Optional | A filter to apply to `loan`-type accounts |
| `investment` | [`InvestmentFilter \| undefined`](../../doc/models/investment-filter.md) | Optional | A filter to apply to `investment`-type accounts |

## Example (as JSON)

```json
{
  "depository": {
    "account_subtypes": [
      "non-taxable brokerage account",
      "other"
    ]
  },
  "credit": {
    "account_subtypes": [
      "ugma",
      "utma",
      "variable annuity"
    ]
  },
  "loan": {
    "account_subtypes": [
      "checking",
      "savings",
      "money market"
    ]
  },
  "investment": {
    "account_subtypes": [
      "consumer",
      "home"
    ]
  }
}
```

