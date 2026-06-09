
# Deposit Switch Create Response

DepositSwitchCreateResponse defines the response schema for `/deposit_switch/create`

## Structure

`DepositSwitchCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositSwitchId` | `string` | Required | ID of the deposit switch. This ID is persisted throughout the lifetime of the deposit switch. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "deposit_switch_id": "deposit_switch_id8",
  "request_id": "request_id8"
}
```

