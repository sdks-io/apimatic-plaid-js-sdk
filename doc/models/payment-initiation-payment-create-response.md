
# Payment Initiation Payment Create Response

PaymentInitiationPaymentCreateResponse defines the response schema for `/payment_initiation/payment/create`

## Structure

`PaymentInitiationPaymentCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Required | A unique ID identifying the payment |
| `status` | `string` | Required | For a payment returned by this endpoint, there is only one possible value:<br><br>`PAYMENT_STATUS_INPUT_NEEDED`: The initial phase of the payment |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "payment_id": "payment_id8",
  "status": "PAYMENT_STATUS_INPUT_NEEDED",
  "request_id": "request_id0"
}
```

