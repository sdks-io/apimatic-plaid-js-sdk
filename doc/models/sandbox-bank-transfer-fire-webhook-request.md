
# Sandbox Bank Transfer Fire Webhook Request

Defines the request schema for `/sandbox/bank_transfer/fire_webhook`

## Structure

`SandboxBankTransferFireWebhookRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `webhook` | `string` | Required | The URL to which the webhook should be sent. |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "secret": "secret6",
  "webhook": "webhook8"
}
```

