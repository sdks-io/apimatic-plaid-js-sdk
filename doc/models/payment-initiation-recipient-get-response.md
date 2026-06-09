
# Payment Initiation Recipient Get Response

PaymentInitiationRecipientGetResponse defines the response schema for `/payment_initiation/recipient/get`

## Structure

`PaymentInitiationRecipientGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `recipientId` | `string` | Required | The ID of the recipient. |
| `name` | `string` | Required | The name of the recipient. |
| `address` | [`PaymentInitiationAddress \| undefined`](../../doc/models/payment-initiation-address.md) | Optional | The optional address of the payment recipient. This object is not currently required to make payments from UK institutions and should not be populated, though may be necessary for future European expansion. |
| `iban` | `string \| null \| undefined` | Optional | The International Bank Account Number (IBAN) for the recipient. |
| `bacs` | [`RecipientBACSNullable \| undefined`](../../doc/models/recipient-bacs-nullable.md) | Optional | - |
| `emiRecipientId` | `string \| null \| undefined` | Optional | The EMI (E-Money Institution) recipient that this recipient is associated with, if any. This EMI recipient is used as an intermediary account to enable Plaid to reconcile the settlement of funds for Payment Initiation requests. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "recipient_id": "recipient_id4",
  "name": "name4",
  "address": {
    "street": [
      "street1"
    ],
    "city": "city6",
    "postal_code": "postal_code8",
    "country": "country0"
  },
  "iban": "iban8",
  "bacs": {
    "account": "account4",
    "sort_code": "sort_code4"
  },
  "emi_recipient_id": "emi_recipient_id4",
  "request_id": "request_id6"
}
```

