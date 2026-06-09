
# Institutions Search Account Filter

*This model accepts additional fields of type unknown.*

## Structure

`InstitutionsSearchAccountFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loan` | [`AccountSubtype[] \| undefined`](../../doc/models/account-subtype.md) | Optional | - |
| `depository` | [`AccountSubtype[] \| undefined`](../../doc/models/account-subtype.md) | Optional | - |
| `credit` | [`AccountSubtype[] \| undefined`](../../doc/models/account-subtype.md) | Optional | - |
| `investment` | [`AccountSubtype[] \| undefined`](../../doc/models/account-subtype.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

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
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

