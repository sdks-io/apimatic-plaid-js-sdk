
# Transactions Update Investments Webhook

Fired when new or canceled transactions have been detected on an investment account.

## Structure

`TransactionsUpdateInvestmentsWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `INVESTMENTS_TRANSACTIONS` |
| `webhookCode` | `string` | Required | `DEFAULT_UPDATE` |
| `itemId` | `string` | Required | The `item_id` of the Item associated with this webhook, warning, or error |
| `error` | [`Error \| undefined`](../../doc/models/error.md) | Optional | We use standard HTTP response codes for success and failure notifications, and our errors are further classified by `error_type`. In general, 200 HTTP codes correspond to success, 40X codes are for developer- or user-related failures, and 50X codes are for Plaid-related issues.  Error fields will be `null` if no error has occurred. |
| `newInvestmentsTransactions` | `number` | Required | The number of new transactions reported since the last time this webhook was fired. |
| `canceledInvestmentsTransactions` | `number` | Required | The number of canceled transactions reported since the last time this webhook was fired. |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type6",
  "webhook_code": "webhook_code6",
  "item_id": "item_id2",
  "error": {
    "error_type": "RECAPTCHA_ERROR",
    "error_code": "error_code6",
    "error_message": "error_message6",
    "display_message": "display_message8",
    "request_id": "request_id4",
    "causes": [
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      }
    ],
    "status": 217.06,
    "documentation_url": "documentation_url6",
    "suggested_action": "suggested_action0"
  },
  "new_investments_transactions": 70.96,
  "canceled_investments_transactions": 22.1
}
```

