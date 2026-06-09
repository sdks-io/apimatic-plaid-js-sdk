
# Transfer User in Request

The legal name and other information for the account holder.

## Structure

`TransferUserInRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `legalName` | `string` | Required | The user's legal name. |
| `phoneNumber` | `string \| undefined` | Optional | The user's phone number. |
| `emailAddress` | `string \| undefined` | Optional | The user's email address. |
| `address` | [`TransferUserAddressInRequest \| undefined`](../../doc/models/transfer-user-address-in-request.md) | Optional | The address associated with the account holder. |

## Example (as JSON)

```json
{
  "legal_name": "legal_name2",
  "phone_number": "phone_number2",
  "email_address": "email_address2",
  "address": {
    "street": "street6",
    "city": "city6",
    "region": "region2",
    "postal_code": "postal_code8",
    "country": "country0"
  }
}
```

