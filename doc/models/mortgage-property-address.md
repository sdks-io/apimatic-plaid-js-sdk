
# Mortgage Property Address

Object containing fields describing property address.

*This model accepts additional fields of type unknown.*

## Structure

`MortgagePropertyAddress`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string \| null` | Required | The city name. |
| `country` | `string \| null` | Required | The ISO 3166-1 alpha-2 country code. |
| `postalCode` | `string \| null` | Required | The five or nine digit postal code. |
| `region` | `string \| null` | Required | The region or state (example "NC"). |
| `street` | `string \| null` | Required | The full street address (example "564 Main Street, Apt 15"). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "city": "city6",
  "country": "country0",
  "postal_code": "postal_code8",
  "region": "region2",
  "street": "street6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

