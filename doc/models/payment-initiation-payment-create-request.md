
# Payment Initiation Payment Create Request

PaymentInitiationPaymentCreateRequest defines the request schema for `/payment_initiation/payment/create`

## Structure

`PaymentInitiationPaymentCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `recipientId` | `string` | Required | The ID of the recipient the payment is for.<br><br>**Constraints**: *Minimum Length*: `1` |
| `reference` | `string` | Required | A reference for the payment. This must be an alphanumeric string with at most 18 characters and must not contain any special characters (since not all institutions support them).<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `18` |
| `amount` | [`PaymentAmount`](../../doc/models/payment-amount.md) | Required | The amount and currency of a payment |
| `schedule` | [`ExternalPaymentScheduleRequest \| undefined`](../../doc/models/external-payment-schedule-request.md) | Optional | The schedule that the payment will be executed on. If a schedule is provided, the payment is automatically set up as a standing order. If no schedule is specified, the payment will be executed only once. |
| `options` | [`PaymentOptions \| undefined`](../../doc/models/payment-options.md) | Optional | Additional payment options |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "secret": "secret6",
  "recipient_id": "recipient_id0",
  "reference": "reference6",
  "amount": {
    "currency": "GBP",
    "value": 52.3
  },
  "schedule": {
    "interval": "WEEKLY",
    "interval_execution_day": 88,
    "start_date": "2016-03-13T12:52:32.123Z",
    "end_date": "2016-03-13T12:52:32.123Z",
    "adjusted_start_date": "2016-03-13T12:52:32.123Z"
  },
  "options": {
    "request_refund_details": false,
    "iban": "iban6",
    "bacs": {
      "account": "account4",
      "sort_code": "sort_code4"
    },
    "emi_account_id": "emi_account_id4"
  }
}
```

