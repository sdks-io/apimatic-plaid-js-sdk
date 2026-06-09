
# Deposit Switch Address Data

The user's address.

*This model accepts additional fields of type unknown.*

## Structure

`DepositSwitchAddressData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string` | Required | The full city name |
| `region` | `string` | Required | The region or state<br>Example: `"NC"` |
| `street` | `string` | Required | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string` | Required | The postal code |
| `country` | `string` | Required | The ISO 3166-1 alpha-2 country code |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "city": "city0",
  "region": "region6",
  "street": "street0",
  "postal_code": "postal_code2",
  "country": "country4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

