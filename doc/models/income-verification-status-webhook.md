
# Income Verification Status Webhook

Fired when the status of an income verification instance has changed. It will typically take several minutes for this webhook to fire after the end user has uploaded their documents in the Document Income flow.

## Structure

`IncomeVerificationStatusWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookType` | `string` | Required | `"INCOME"` |
| `webhookCode` | `string` | Required | `income_verification` |
| `incomeVerificationId` | `string` | Required | The `income_verification_id` of the verification instance whose status is being reported. |
| `verificationStatus` | `string` | Required | `VERIFICATION_STATUS_PROCESSING_COMPLETE`: The income verification status processing has completed.<br><br>`VERIFICATION_STATUS_UPLOAD_ERROR`: An upload error occurred when the end user attempted to upload their verification documentation.<br><br>`VERIFICATION_STATUS_INVALID_TYPE`: The end user attempted to upload verification documentation in an unsupported file format.<br><br>`VERIFICATION_STATUS_DOCUMENT_REJECTED`: The documentation uploaded by the end user was recognized as a supported file format, but not recognized as a valid paystub.<br><br>`VERIFICATION_STATUS_PROCESSING_FAILED`: A failure occurred when attempting to process the verification documentation. |

## Example (as JSON)

```json
{
  "webhook_type": "webhook_type4",
  "webhook_code": "webhook_code4",
  "income_verification_id": "income_verification_id8",
  "verification_status": "verification_status0"
}
```

