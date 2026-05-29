
# Account Filter

Enumerates the account subtypes that the application wishes for the user to be able to select from. For more details refer to Plaid documentation on account filters.

*This model accepts additional fields of type unknown.*

## Structure

`AccountFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depository` | `string[] \| undefined` | Optional | A list of account subtypes to be filtered. |
| `credit` | `string[] \| undefined` | Optional | A list of account subtypes to be filtered. |
| `loan` | `string[] \| undefined` | Optional | A list of account subtypes to be filtered. |
| `investment` | `string[] \| undefined` | Optional | A list of account subtypes to be filtered. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "depository": [
    "depository9"
  ],
  "credit": [
    "credit0",
    "credit1",
    "credit2"
  ],
  "loan": [
    "loan5",
    "loan4",
    "loan3"
  ],
  "investment": [
    "investment9",
    "investment0"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

