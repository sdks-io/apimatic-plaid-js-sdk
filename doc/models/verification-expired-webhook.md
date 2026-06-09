
# Verification Expired Webhook

Fired when an Item was not verified via automated micro-deposits after ten days since the automated micro-deposit was made.

## Structure

`VerificationExpiredWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `AUTH` |
| `webhookCode` | `string` | Required | `VERIFICATION_EXPIRED` |
| `itemId` | `string` | Required | The `item_id` of the Item associated with this webhook, warning, or error |
| `accountId` | `string` | Required | The `account_id` of the account associated with the webhook |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type0",
  "webhook_code": "webhook_code0",
  "item_id": "item_id4",
  "account_id": "account_id8"
}
```

