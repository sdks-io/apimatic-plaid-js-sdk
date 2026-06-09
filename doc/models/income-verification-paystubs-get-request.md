
# Income Verification Paystubs Get Request

IncomeVerificationPaystubsGetRequest defines the request schema for `/income/verification/paystubs/get`.

## Structure

`IncomeVerificationPaystubsGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `incomeVerificationId` | `string \| null \| undefined` | Optional | The ID of the verification for which to get paystub information. |
| `accessToken` | `string \| null \| undefined` | Optional | The access token associated with the Item data is being requested for. |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "secret": "secret4",
  "income_verification_id": "income_verification_id4",
  "access_token": "access_token6"
}
```

