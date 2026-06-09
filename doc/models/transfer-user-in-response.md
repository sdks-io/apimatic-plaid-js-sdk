
# Transfer User in Response

The legal name and other information for the account holder.

## Structure

`TransferUserInResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `legalName` | `string` | Required | The user's legal name. |
| `phoneNumber` | `string \| null` | Required | The user's phone number. |
| `emailAddress` | `string \| null` | Required | The user's email address. |
| `address` | [`TransferUserAddressInResponse`](../../doc/models/transfer-user-address-in-response.md) | Required | The address associated with the account holder. |

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

