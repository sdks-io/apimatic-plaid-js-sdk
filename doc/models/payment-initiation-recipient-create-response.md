
# Payment Initiation Recipient Create Response

PaymentInitiationRecipientCreateResponse defines the response schema for `/payment_initation/recipient/create`

*This model accepts additional fields of type unknown.*

## Structure

`PaymentInitiationRecipientCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `recipientId` | `string` | Required | A unique ID identifying the recipient |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "recipient_id": "recipient_id4",
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

