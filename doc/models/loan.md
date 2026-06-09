
# Loan

A filter to apply to `loan`-type accounts

## Structure

`Loan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountSubtypes` | [`AccountSubtypeEnum[] \| undefined`](../../doc/models/account-subtype-enum.md) | Optional | An array of account subtypes to display in Link. If not specified, all account subtypes will be shown. For a full list of valid types and subtypes, see the [Account schema](https://plaid.com/docs/api/accounts#accounts-schema). |

## Example (as JSON)

```json
{
  "account_subtypes": [
    "ugma",
    "utma",
    "variable annuity"
  ]
}
```

