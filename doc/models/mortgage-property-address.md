
# Mortgage Property Address

Object containing fields describing property address.

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

## Example (as JSON)

```json
{
  "city": "city6",
  "country": "country0",
  "postal_code": "postal_code8",
  "region": "region2",
  "street": "street6"
}
```

