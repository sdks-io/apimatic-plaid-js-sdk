
# Item Status Last Webhook

Information about the last webhook fired for the Item.

## Structure

`ItemStatusLastWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sentAt` | `string \| null \| undefined` | Optional | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) timestamp of when the webhook was fired. |
| `codeSent` | `string \| null \| undefined` | Optional | The last webhook code sent. |

## Example (as JSON)

```json
{
  "sent_at": "2016-03-13T12:52:32.123Z",
  "code_sent": "code_sent0"
}
```

