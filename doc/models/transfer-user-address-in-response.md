
# Transfer User Address in Response

The address associated with the account holder.

*This model accepts additional fields of type unknown.*

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
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "street": "street8",
  "city": "city2",
  "region": "region4",
  "postal_code": "postal_code0",
  "country": "country2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

