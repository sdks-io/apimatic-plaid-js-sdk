
# Pending Expiration Webhook

Fired when an Item’s access consent is expiring in 7 days. Some Items have explicit expiration times and we try to relay this when possible to reduce service disruption. This can be resolved by having the user go through Link’s update mode.

## Structure

`PendingExpirationWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `ITEM` |
| `webhookCode` | `string` | Required | `PENDING_EXPIRATION` |
| `itemId` | `string` | Required | The `item_id` of the Item associated with this webhook, warning, or error |
| `consentExpirationTime` | `string` | Required | The date and time at which the Item's access consent will expire, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type4",
  "webhook_code": "webhook_code6",
  "item_id": "item_id0",
  "consent_expiration_time": "2016-03-13T12:52:32.123Z"
}
```

