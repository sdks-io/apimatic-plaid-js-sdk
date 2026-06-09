
# Asset Report Audit Copy Create Response

AssetReportAuditCopyCreateResponse defines the response schema for `/asset_report/audit_copy/get`

## Structure

`AssetReportAuditCopyCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auditCopyToken` | `string` | Required | A token that can be shared with a third party auditor to allow them to obtain access to the Asset Report. This token should be stored securely. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "audit_copy_token": "audit_copy_token8",
  "request_id": "request_id2"
}
```

