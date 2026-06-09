
# Payment Initiation Payment Get Request

PaymentInitiationPaymentGetRequest defines the request schema for `/payment_initiation/payment/get`

## Structure

`PaymentInitiationPaymentGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `paymentId` | `string` | Required | The `payment_id` returned from `/payment_initiation/payment/create`.<br><br>**Constraints**: *Minimum Length*: `1` |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "payment_id": "payment_id6"
}
```

