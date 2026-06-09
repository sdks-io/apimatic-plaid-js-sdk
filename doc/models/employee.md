
# Employee

Data about the employee.

## Structure

`Employee`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| null` | Required | The name of the employee. |
| `address` | [`Address2`](../../doc/models/address-2.md) | Required | - |
| `maritalStatus` | `string \| null \| undefined` | Optional | Marital status of the employee. |
| `taxpayerId` | [`TaxpayerID \| undefined`](../../doc/models/taxpayer-id.md) | Optional | - |

## Example (as JSON)

```json
{
  "name": "name6",
  "address": {
    "city": "city6",
    "street": "street6",
    "line1": "line18",
    "line2": "line20",
    "postal_code": "postal_code8"
  },
  "marital_status": "marital_status4",
  "taxpayer_id": {
    "id_type": "id_type8",
    "last_4_digits": "last_4_digits6"
  }
}
```

