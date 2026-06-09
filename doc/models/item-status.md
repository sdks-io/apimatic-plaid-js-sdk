
# Item Status

An object with information about the status of the Item.

## Structure

`ItemStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `investments` | [`ItemStatusInvestments \| undefined`](../../doc/models/item-status-investments.md) | Optional | Information about the last successful and failed investments update for the Item. |
| `transactions` | [`ItemStatusTransactions \| undefined`](../../doc/models/item-status-transactions.md) | Optional | Information about the last successful and failed transactions update for the Item. |
| `lastWebhook` | [`ItemStatusLastWebhook \| undefined`](../../doc/models/item-status-last-webhook.md) | Optional | Information about the last webhook fired for the Item. |

## Example (as JSON)

```json
{
  "investments": {
    "last_successful_update": "2016-03-13T12:52:32.123Z",
    "last_failed_update": "2016-03-13T12:52:32.123Z"
  },
  "transactions": {
    "last_successful_update": "2016-03-13T12:52:32.123Z",
    "last_failed_update": "2016-03-13T12:52:32.123Z"
  },
  "last_webhook": {
    "sent_at": "2016-03-13T12:52:32.123Z",
    "code_sent": "code_sent2"
  }
}
```

