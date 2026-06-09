
# Payment Initiation Payment List Response

PaymentInitiationPaymentListResponse defines the response schema for `/payment_initiation/payment/list`

## Structure

`PaymentInitiationPaymentListResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payments` | [`PaymentInitiationPayment[]`](../../doc/models/payment-initiation-payment.md) | Required | An array of payments that have been created, associated with the given `client_id`. |
| `nextCursor` | `string \| null` | Required | The value that, when used as the optional `cursor` parameter to `/payment_initiation/payment/list`, will return the next unreturned payment as its first payment. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "payments": [
    {
      "payment_id": "payment_id2",
      "amount": {
        "currency": "GBP",
        "value": 52.3
      },
      "status": "PAYMENT_STATUS_INSUFFICIENT_FUNDS",
      "recipient_id": "recipient_id8",
      "reference": "reference2",
      "adjusted_reference": "adjusted_reference6",
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
      "iban": "iban6",
      "initiated_refunds": [
        {
          "refund_id": "refund_id0",
          "amount": {
            "currency": "GBP",
            "value": 52.3
          },
          "status": "INITIATED",
          "last_status_update": "2016-03-13T12:52:32.123Z"
        },
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
      "emi_account_id": "emi_account_id4"
    }
  ],
  "next_cursor": "2016-03-13T12:52:32.123Z",
  "request_id": "request_id2"
}
```

