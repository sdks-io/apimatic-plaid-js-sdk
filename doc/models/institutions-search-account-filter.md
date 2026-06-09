
# Institutions Search Account Filter

## Structure

`InstitutionsSearchAccountFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loan` | [`AccountSubtypeEnum[] \| undefined`](../../doc/models/account-subtype-enum.md) | Optional | - |
| `depository` | [`AccountSubtypeEnum[] \| undefined`](../../doc/models/account-subtype-enum.md) | Optional | - |
| `credit` | [`AccountSubtypeEnum[] \| undefined`](../../doc/models/account-subtype-enum.md) | Optional | - |
| `investment` | [`AccountSubtypeEnum[] \| undefined`](../../doc/models/account-subtype-enum.md) | Optional | - |

## Example (as JSON)

```json
{
  "loan": [
    "cd",
    "paypal"
  ],
  "depository": [
    "retirement",
    "roth",
    "roth 401k"
  ],
  "credit": [
    "rrsp",
    "sep ira"
  ],
  "investment": [
    "construction"
  ]
}
```

