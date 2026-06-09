
# Assets Product Ready Webhook

Fired when the Asset Report has been generated and `/asset_report/get` is ready to be called.  If you attempt to retrieve an Asset Report before this webhook has fired, you’ll receive a response with the HTTP status code 400 and a Plaid error code of `PRODUCT_NOT_READY`.

## Structure

`AssetsProductReadyWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `ASSETS` |
| `webhookCode` | `string` | Required | `PRODUCT_READY` |
| `assetReportId` | `string` | Required | The `asset_report_id` that can be provided to `/asset_report/get` to retrieve the Asset Report. |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type8",
  "webhook_code": "webhook_code2",
  "asset_report_id": "asset_report_id6"
}
```

