
# Deposit Switch Target User

## Structure

`DepositSwitchTargetUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `givenName` | `string` | Required | The given name (first name) of the user. |
| `familyName` | `string` | Required | The family name (last name) of the user. |
| `phone` | `string` | Required | The phone number of the user. The endpoint can accept a variety of phone number formats, including E.164. |
| `email` | `string` | Required | The email address of the user. |
| `address` | [`DepositSwitchAddressData \| undefined`](../../doc/models/deposit-switch-address-data.md) | Optional | The user's address. |
| `taxPayerId` | `string \| undefined` | Optional | The taxpayer ID of the user, generally their SSN, EIN, or TIN. |

## Example (as JSON)

```json
{
  "given_name": "given_name8",
  "family_name": "family_name0",
  "phone": "phone4",
  "email": "email0",
  "address": {
    "city": "city6",
    "region": "region2",
    "street": "street6",
    "postal_code": "postal_code8",
    "country": "country0"
  },
  "tax_payer_id": "tax_payer_id4"
}
```

