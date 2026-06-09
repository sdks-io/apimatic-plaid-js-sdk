
# Sandbox Income Fire Webhook Request

SandboxIncomeFireWebhookRequest defines the request schema for `/sandbox/income/fire_webhook`

## Structure

`SandboxIncomeFireWebhookRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `incomeVerificationId` | `string` | Required | The ID of the verification. |
| `webhook` | `string` | Required | The URL to which the webhook should be sent. |
| `verificationStatus` | [`VerificationStatus3Enum`](../../doc/models/verification-status-3-enum.md) | Required | `VERIFICATION_STATUS_PROCESSING_COMPLETE`: The income verification status processing has completed.<br><br>`VERIFICATION_STATUS_DOCUMENT_REJECTED`: The documentation uploaded by the end user was recognized as a supported file format, but not recognized as a valid paystub.<br><br>`VERIFICATION_STATUS_PROCESSING_FAILED`: A failure occurred when attempting to process the verification documentation. |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret8",
  "income_verification_id": "income_verification_id0",
  "webhook": "webhook0",
  "verification_status": "VERIFICATION_STATUS_DOCUMENT_REJECTED"
}
```

