
# Automatically Verified Webhook

Fired when an Item is verified via automated micro-deposits. We recommend communicating to your users when this event is received to notify them that their account is verified and ready for use.

*This model accepts additional fields of type unknown.*

## Structure

`AutomaticallyVerifiedWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `AUTH` |
| `webhookCode` | `string` | Required | `AUTOMATICALLY_VERIFIED` |
| `accountId` | `string` | Required | The `account_id` of the account associated with the webhook |
| `itemId` | `string` | Required | The `item_id` of the Item associated with this webhook, warning, or error |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type2",
  "webhook_code": "webhook_code8",
  "account_id": "account_id0",
  "item_id": "item_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

