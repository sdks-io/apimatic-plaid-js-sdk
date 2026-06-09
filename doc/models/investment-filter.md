
# Investment Filter

A filter to apply to `investment`-type accounts

## Structure

`InvestmentFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountSubtypes` | [`AccountSubtypeEnum[]`](../../doc/models/account-subtype-enum.md) | Required | An array of account subtypes to display in Link. If not specified, all account subtypes will be shown. For a full list of valid types and subtypes, see the [Account schema](https://plaid.com/docs/api/accounts#accounts-schema). |

## Example (as JSON)

```json
{
  "account_subtypes": [
    "money market",
    "prepaid"
  ]
}
```

