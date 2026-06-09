
# Servicer Address Data

The address of the student loan servicer. This is generally the remittance address to which payments should be sent.

## Structure

`ServicerAddressData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string \| null` | Required | The full city name |
| `region` | `string \| null` | Required | The region or state<br>Example: `"NC"` |
| `street` | `string \| null` | Required | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string \| null` | Required | The postal code |
| `country` | `string \| null` | Required | The ISO 3166-1 alpha-2 country code |

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

