
# Address Data 1

Data about the components comprising an address.

## Structure

`AddressData1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string \| undefined` | Optional | The full city name |
| `region` | `string \| null \| undefined` | Optional | The region or state<br>Example: `"NC"` |
| `street` | `string \| undefined` | Optional | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string \| null \| undefined` | Optional | The postal code |
| `country` | `string \| null \| undefined` | Optional | The ISO 3166-1 alpha-2 country code |

## Example (as JSON)

```json
{
  "city": "city4",
  "region": "region2",
  "street": "street6",
  "postal_code": "postal_code8",
  "country": "country0"
}
```

