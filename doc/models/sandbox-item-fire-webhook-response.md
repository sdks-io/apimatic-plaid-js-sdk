
# Sandbox Item Fire Webhook Response

SandboxItemFireWebhookResponse defines the response schema for `/sandbox/item/fire_webhook`

*This model accepts additional fields of type unknown.*

## Structure

`SandboxItemFireWebhookResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookFired` | `boolean` | Required | Value is `true`  if the test` webhook_code`  was successfully fired. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "webhook_fired": false,
  "request_id": "request_id4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

