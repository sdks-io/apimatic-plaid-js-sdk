
# Payment Initiation Recipient Get Request

PaymentInitiationRecipientGetRequest defines the request schema for `/payment_initiation/recipient/get`

## Structure

`PaymentInitiationRecipientGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `recipientId` | `string` | Required | The ID of the recipient<br><br>**Constraints**: *Minimum Length*: `1` |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret8",
  "recipient_id": "recipient_id4"
}
```

