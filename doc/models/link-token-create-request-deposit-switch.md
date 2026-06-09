
# Link Token Create Request Deposit Switch

Specifies options for initializing Link for use with the Deposit Switch (beta) product. This field is required if `deposit_switch` is included in the `products` array.

## Structure

`LinkTokenCreateRequestDepositSwitch`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositSwitchId` | `string` | Required | The `deposit_switch_id` provided by the `/deposit_switch/create` endpoint. |

## Example (as JSON)

```json
{
  "deposit_switch_id": "deposit_switch_id0"
}
```

