
# Payment Initiation Payment Get Response

PaymentInitiationPaymentGetResponse defines the response schema for `/payment_initation/payment/get`

## Structure

`PaymentInitiationPaymentGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Required | The ID of the payment. Like all Plaid identifiers, the `payment_id` is case sensitive. |
| `amount` | [`PaymentAmount`](../../doc/models/payment-amount.md) | Required | The amount and currency of a payment |
| `status` | [`Status3Enum`](../../doc/models/status-3-enum.md) | Required | The status of the payment.<br><br>`PAYMENT_STATUS_INPUT_NEEDED`: This is the initial state of all payments. It indicates that the payment is waiting on user input to continue processing. A payment may re-enter this state later on if further input is needed.<br><br>`PAYMENT_STATUS_PROCESSING`: The payment is currently being processed. The payment will automatically exit this state when processing is complete.<br><br>`PAYMENT_STATUS_INITIATED`: The payment has been successfully initiated and is considered complete.<br><br>`PAYMENT_STATUS_COMPLETED`: Indicates that the standing order has been successfully established. This state is only used for standing orders.<br><br>`PAYMENT_STATUS_INSUFFICIENT_FUNDS`: The payment has failed due to insufficient funds.<br><br>`PAYMENT_STATUS_FAILED`: The payment has failed to be initiated. This error is retryable once the root cause is resolved.<br><br>`PAYMENT_STATUS_BLOCKED`: The payment has been blocked. This is a retryable error.<br><br>`PAYMENT_STATUS_UNKNOWN`: The payment status is unknown. |
| `recipientId` | `string` | Required | The ID of the recipient |
| `reference` | `string` | Required | A reference for the payment. |
| `adjustedReference` | `string \| null \| undefined` | Optional | The value of the reference sent to the bank after adjustment to pass bank validation rules. |
| `lastStatusUpdate` | `string` | Required | The date and time of the last time the `status` was updated, in IS0 8601 format |
| `schedule` | [`ExternalPaymentScheduleGet \| undefined`](../../doc/models/external-payment-schedule-get.md) | Optional | The schedule that the payment will be executed on. If a schedule is provided, the payment is automatically set up as a standing order. If no schedule is specified, the payment will be executed only once. |
| `refundDetails` | [`ExternalPaymentRefundDetails \| undefined`](../../doc/models/external-payment-refund-details.md) | Optional | - |
| `bacs` | [`SenderBACSNullable`](../../doc/models/sender-bacs-nullable.md) | Required | - |
| `iban` | `string \| null` | Required | The International Bank Account Number (IBAN) for the sender, if specified in the `/payment_initiation/payment/create` call. |
| `initiatedRefunds` | [`PaymentInitiationRefund[] \| undefined`](../../doc/models/payment-initiation-refund.md) | Optional | Initiated refunds associated with the payment. |
| `emiAccountId` | `string \| null \| undefined` | Optional | The EMI (E-Money Institution) account that this payment is associated with, if any. This EMI account is used as an intermediary account to enable Plaid to reconcile the settlement of funds for Payment Initiation requests.<br><br>**Constraints**: *Minimum Length*: `1` |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "payment_id": "payment_id8",
  "amount": {
    "currency": "GBP",
    "value": 52.3
  },
  "status": "PAYMENT_STATUS_INITIATED",
  "recipient_id": "recipient_id2",
  "reference": "reference6",
  "adjusted_reference": "adjusted_reference2",
  "last_status_update": "2016-03-13T12:52:32.123Z",
  "schedule": {
    "interval": "WEEKLY",
    "interval_execution_day": 88,
    "start_date": "2016-03-13T12:52:32.123Z",
    "end_date": "2016-03-13T12:52:32.123Z",
    "adjusted_start_date": "2016-03-13T12:52:32.123Z"
  },
  "refund_details": {
    "name": "name8",
    "iban": "iban2",
    "bacs": {
      "account": "account4",
      "sort_code": "sort_code4"
    }
  },
  "bacs": {
    "account": "account4",
    "sort_code": "sort_code4"
  },
  "iban": "iban2",
  "initiated_refunds": [
    {
      "refund_id": "refund_id0",
      "amount": {
        "currency": "GBP",
        "value": 52.3
      },
      "status": "INITIATED",
      "last_status_update": "2016-03-13T12:52:32.123Z"
    }
  ],
  "emi_account_id": "emi_account_id8",
  "request_id": "request_id0"
}
```

