
# Bank Transfers Events Update Webhook

Fired when new bank transfer events are available. Receiving this webhook indicates you should fetch the new events from `/bank_transfer/event/sync`.

## Structure

`BankTransfersEventsUpdateWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `BANK_TRANSFERS` |
| `webhookCode` | `string` | Required | `BANK_TRANSFERS_EVENTS_UPDATE` |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type0",
  "webhook_code": "webhook_code0"
}
```

