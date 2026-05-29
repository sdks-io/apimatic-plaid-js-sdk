
# Initial Update Webhook

Fired when an Item's initial transaction pull is completed. Once this webhook has been fired, transaction data for the most recent 30 days can be fetched for the Item. If [Account Select v2](https://plaid.com/docs/link/customization/#account-select) is enabled, this webhook will also be fired if account selections for the Item are updated, with `num_transactions` set to the number of net new transactions pulled after the account selection update.

*This model accepts additional fields of type unknown.*

## Structure

`InitialUpdateWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `TRANSACTIONS` |
| `webhookCode` | `string` | Required | `INITIAL_UPDATE` |
| `error` | `string \| null \| undefined` | Optional | The error code associated with the webhook. |
| `newTransactions` | `number` | Required | The number of new, unfetched transactions available. |
| `itemId` | `string` | Required | The `item_id` of the Item associated with this webhook, warning, or error |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type2",
  "webhook_code": "webhook_code2",
  "error": "error2",
  "new_transactions": 168.68,
  "item_id": "item_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

