
# Address Data Nullable

*This model accepts additional fields of type unknown.*

## Structure

`AddressDataNullable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string` | Required | The full city name |
| `region` | `string \| null` | Required | The region or state<br>Example: `"NC"` |
| `street` | `string` | Required | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string \| null` | Required | The postal code |
| `country` | `string \| null` | Required | The ISO 3166-1 alpha-2 country code |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "city": "city2",
  "region": "region8",
  "street": "street2",
  "postal_code": "postal_code4",
  "country": "country6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

