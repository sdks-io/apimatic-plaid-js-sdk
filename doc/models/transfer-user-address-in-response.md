
# Transfer User Address in Response

The address associated with the account holder.

## Structure

`TransferUserAddressInResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `street` | `string \| null` | Required | The street number and name (i.e., "100 Market St."). |
| `city` | `string \| null` | Required | Ex. "San Francisco" |
| `region` | `string \| null` | Required | The state or province (e.g., "California"). |
| `postalCode` | `string \| null` | Required | The postal code (e.g., "94103"). |
| `country` | `string \| null` | Required | A two-letter country code (e.g., "US"). |

## Example (as JSON)

```json
{
  "street": "street8",
  "city": "city2",
  "region": "region4",
  "postal_code": "postal_code0",
  "country": "country2"
}
```

