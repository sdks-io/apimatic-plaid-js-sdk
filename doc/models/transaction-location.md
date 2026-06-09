
# Transaction Location

A representation of where a transaction took place

## Structure

`TransactionLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address` | `string \| null` | Required | The street address where the transaction occurred. |
| `city` | `string \| null` | Required | The city where the transaction occurred. |
| `region` | `string \| null` | Required | The region or state where the transaction occurred. |
| `postalCode` | `string \| null` | Required | The postal code where the transaction occurred. |
| `country` | `string \| null` | Required | The ISO 3166-1 alpha-2 country code where the transaction occurred. |
| `lat` | `number \| null` | Required | The latitude where the transaction occurred. |
| `lon` | `number \| null` | Required | The longitude where the transaction occurred. |
| `storeNumber` | `string \| null` | Required | The merchant defined store number where the transaction occurred. |

## Example (as JSON)

```json
{
  "address": "address8",
  "city": "city8",
  "region": "region8",
  "postal_code": "postal_code4",
  "country": "country6",
  "lat": 198.3,
  "lon": 224.6,
  "store_number": "store_number8"
}
```

