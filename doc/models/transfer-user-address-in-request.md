
# Transfer User Address in Request

The address associated with the account holder.

*This model accepts additional fields of type unknown.*

## Structure

`TransferUserAddressInRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `street` | `string \| undefined` | Optional | The street number and name (i.e., "100 Market St."). |
| `city` | `string \| undefined` | Optional | Ex. "San Francisco" |
| `region` | `string \| undefined` | Optional | The state or province (e.g., "California"). |
| `postalCode` | `string \| undefined` | Optional | The postal code (e.g., "94103"). |
| `country` | `string \| undefined` | Optional | A two-letter country code (e.g., "US"). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "street": "street0",
  "city": "city0",
  "region": "region6",
  "postal_code": "postal_code2",
  "country": "country4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

