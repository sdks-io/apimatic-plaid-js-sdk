
# Deposit Switch Address Data

The user's address.

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

## Example (as JSON)

```json
{
  "city": "city0",
  "region": "region6",
  "street": "street0",
  "postal_code": "postal_code2",
  "country": "country4"
}
```

