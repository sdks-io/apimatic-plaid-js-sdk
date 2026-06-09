
# Sandbox Bank Transfer Fire Webhook Response

Defines the response schema for `/sandbox/bank_transfer/fire_webhook`

## Structure

`SandboxBankTransferFireWebhookResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "request_id": "request_id4"
}
```

