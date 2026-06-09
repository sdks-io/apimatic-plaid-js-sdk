
# Address Data

Data about the components comprising an address.

## Structure

`AddressData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string` | Required | The full city name |
| `region` | `string \| null` | Required | The region or state<br>Example: `"NC"` |
| `street` | `string` | Required | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string \| null` | Required | The postal code |
| `country` | `string \| null` | Required | The ISO 3166-1 alpha-2 country code |

## Example (as JSON)

```json
{
  "city": "city4",
  "region": "region0",
  "street": "street4",
  "postal_code": "postal_code6",
  "country": "country8"
}
```

