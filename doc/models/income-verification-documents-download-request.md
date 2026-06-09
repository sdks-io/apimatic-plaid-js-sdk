
# Income Verification Documents Download Request

IncomeVerificationDocumentsDownloadRequest defines the request schema for `/income/verification/documents/download`.

*This model accepts additional fields of type unknown.*

## Structure

`IncomeVerificationDocumentsDownloadRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `incomeVerificationId` | `string \| null \| undefined` | Optional | The ID of the verification. |
| `accessToken` | `string \| null \| undefined` | Optional | The access token associated with the Item data is being requested for. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "income_verification_id": "income_verification_id8",
  "access_token": "access_token2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

