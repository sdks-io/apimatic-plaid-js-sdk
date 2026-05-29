
# Asset Report Audit Copy Remove Response

AssetReportAuditCopyRemoveResponse defines the response schema for `/asset_report/audit_copy/remove`

*This model accepts additional fields of type unknown.*

## Structure

`AssetReportAuditCopyRemoveResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `removed` | `boolean` | Required | `true` if the Audit Copy was successfully removed. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "removed": false,
  "request_id": "request_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

