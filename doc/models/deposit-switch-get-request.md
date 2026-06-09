
# Deposit Switch Get Request

DepositSwitchGetRequest defines the request schema for `/deposit_switch/get`

## Structure

`DepositSwitchGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `depositSwitchId` | `string` | Required | The ID of the deposit switch |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "deposit_switch_id": "deposit_switch_id4"
}
```

