
# Deposit Switch State Update Webhook

Fired when the status of a deposit switch request has changed.

## Structure

`DepositSwitchStateUpdateWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string \| undefined` | Optional | `"DEPOSIT_SWITCH"` |
| `webhookCode` | `string \| undefined` | Optional | `"SWITCH_STATE_UPDATE"` |
| `state` | `string \| undefined` | Optional | The state, or status, of the deposit switch.<br><br>`initialized`: The deposit switch has been initialized with the user entering the information required to submit the deposit switch request.<br><br>`processing`: The deposit switch request has been submitted and is being processed.<br><br>`completed`: The user's employer has fulfilled and completed the deposit switch request.<br><br>`error`: There was an error processing the deposit switch request.<br><br>For more information, see the [Deposit Switch API reference](/docs/api/products#deposit_switchget). |
| `depositSwitchId` | `string \| undefined` | Optional | The ID of the deposit switch. |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type8",
  "webhook_code": "webhook_code8",
  "state": "state0",
  "deposit_switch_id": "deposit_switch_id2"
}
```

