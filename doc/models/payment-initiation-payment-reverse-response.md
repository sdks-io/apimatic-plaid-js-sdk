
# Payment Initiation Payment Reverse Response

PaymentInitiationPaymentReverseResponse defines the response schema for `/payment_initation/payment/reverse`

## Structure

`PaymentInitiationPaymentReverseResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refundId` | `string` | Required | A unique ID identifying the refund |
| `status` | [`Status2Enum`](../../doc/models/status-2-enum.md) | Required | The status of the refund.<br><br>`PROCESSING`: The refund is currently being processed. The refund will automatically exit this state when processing is complete.<br><br>`INITIATED`: The refund has been successfully initiated.<br><br>`EXECUTED`: Indicates that the refund has been successfully executed.<br><br>`FAILED`: The refund has failed to be executed. This error is retryable once the root cause is resolved. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "refund_id": "refund_id2",
  "status": "PROCESSING",
  "request_id": "request_id0"
}
```

