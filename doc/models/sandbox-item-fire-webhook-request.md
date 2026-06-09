
# Sandbox Item Fire Webhook Request

SandboxItemFireWebhookRequest defines the request schema for `/sandbox/item/fire_webhook`

## Structure

`SandboxItemFireWebhookRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `webhookCode` | `string` | Required | The following values for `webhook_code` are supported:<br><br>* `DEFAULT_UPDATE` |

## Example (as JSON)

```json
{
  "access_token": "access_token6",
  "webhook_code": "DEFAULT_UPDATE",
  "client_id": "client_id0",
  "secret": "secret6"
}
```

