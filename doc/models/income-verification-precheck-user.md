
# Income Verification Precheck User

## Structure

`IncomeVerificationPrecheckUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firstName` | `string \| null \| undefined` | Optional | The user's first name |
| `lastName` | `string \| null \| undefined` | Optional | The user's last name |
| `emailAddress` | `string \| null \| undefined` | Optional | The user's email address |
| `homeAddress` | [`AddressData1 \| undefined`](../../doc/models/address-data-1.md) | Optional | Data about the components comprising an address. |

## Example (as JSON)

```json
{
  "first_name": "first_name4",
  "last_name": "last_name2",
  "email_address": "email_address8",
  "home_address": {
    "city": "city0",
    "region": "region6",
    "street": "street0",
    "postal_code": "postal_code2",
    "country": "country4"
  }
}
```

