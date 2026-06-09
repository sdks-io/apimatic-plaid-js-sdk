
# Address Nullable

## Structure

`AddressNullable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`AddressData`](../../doc/models/address-data.md) | Required | Data about the components comprising an address. |
| `primary` | `boolean \| undefined` | Optional | When `true`, identifies the address as the primary address on an account. |

## Example (as JSON)

```json
{
  "data": {
    "city": "city0",
    "region": "region6",
    "street": "street0",
    "postal_code": "postal_code2",
    "country": "country4"
  },
  "primary": false
}
```

