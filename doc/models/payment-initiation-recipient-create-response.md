
# Payment Initiation Recipient Create Response

PaymentInitiationRecipientCreateResponse defines the response schema for `/payment_initation/recipient/create`

## Structure

`PaymentInitiationRecipientCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `recipientId` | `string` | Required | A unique ID identifying the recipient |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "recipient_id": "recipient_id4",
  "request_id": "request_id2"
}
```

