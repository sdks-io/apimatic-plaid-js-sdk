
# Asset Report Remove Response

AssetReportRemoveResponse defines the response schema for `/asset_report/remove`

## Structure

`AssetReportRemoveResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `removed` | `boolean` | Required | `true` if the Asset Report was successfully removed. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "removed": false,
  "request_id": "request_id6"
}
```

