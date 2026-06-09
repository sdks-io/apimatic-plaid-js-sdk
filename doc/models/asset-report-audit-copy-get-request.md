
# Asset Report Audit Copy Get Request

AssetReportAuditCopyGetRequest defines the request schema for `/asset_report/audit_copy/get`

## Structure

`AssetReportAuditCopyGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `auditCopyToken` | `string` | Required | The `audit_copy_token` granting access to the Audit Copy you would like to get. |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "audit_copy_token": "audit_copy_token4"
}
```

