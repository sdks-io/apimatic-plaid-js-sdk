
# Account Filters Response

The `account_filters` specified in the original call to `/link/token/create`.

*This model accepts additional fields of type unknown.*

## Structure

`AccountFiltersResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depository` | [`DepositoryFilter \| undefined`](../../doc/models/depository-filter.md) | Optional | A filter to apply to `depository`-type accounts |
| `credit` | [`CreditFilter \| undefined`](../../doc/models/credit-filter.md) | Optional | A filter to apply to `credit`-type accounts |
| `loan` | [`LoanFilter \| undefined`](../../doc/models/loan-filter.md) | Optional | A filter to apply to `loan`-type accounts |
| `investment` | [`InvestmentFilter \| undefined`](../../doc/models/investment-filter.md) | Optional | A filter to apply to `investment`-type accounts |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "depository": {
    "account_subtypes": [
      "non-taxable brokerage account",
      "other"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "credit": {
    "account_subtypes": [
      "ugma",
      "utma",
      "variable annuity"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "loan": {
    "account_subtypes": [
      "checking",
      "savings",
      "money market"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "investment": {
    "account_subtypes": [
      "consumer",
      "home"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

