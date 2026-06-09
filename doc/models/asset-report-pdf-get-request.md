
# Asset Report PDF Get Request

AssetReportPDFGetRequest defines the request schema for `/asset_report/pdf/get`

## Structure

`AssetReportPDFGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `assetReportToken` | `string` | Required | A token that can be provided to endpoints such as `/asset_report/get` or `/asset_report/pdf/get` to fetch or update an Asset Report. |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "asset_report_token": "asset_report_token6"
}
```

