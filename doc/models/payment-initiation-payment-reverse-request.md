
# Payment Initiation Payment Reverse Request

PaymentInitiationPaymentReverseRequest defines the request schema for `/payment_initiation/payment/reverse`

## Structure

`PaymentInitiationPaymentReverseRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `paymentId` | `string` | Required | The ID of the payment to reverse<br><br>**Constraints**: *Minimum Length*: `1` |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret2",
  "payment_id": "payment_id2"
}
```

