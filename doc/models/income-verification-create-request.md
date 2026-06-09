
# Income Verification Create Request

IncomeVerificationCreateRequest defines the request schema for `/income/verification/create`

## Structure

`IncomeVerificationCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `webhook` | `string` | Required | The URL endpoint to which Plaid should send webhooks related to the progress of the income verification process. |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret2",
  "webhook": "webhook0"
}
```

