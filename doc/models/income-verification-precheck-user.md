
# Income Verification Precheck User

*This model accepts additional fields of type unknown.*

## Structure

`IncomeVerificationPrecheckUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firstName` | `string \| null \| undefined` | Optional | The user's first name |
| `lastName` | `string \| null \| undefined` | Optional | The user's last name |
| `emailAddress` | `string \| null \| undefined` | Optional | The user's email address |
| `homeAddress` | [`AddressData1 \| undefined`](../../doc/models/address-data-1.md) | Optional | Data about the components comprising an address. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

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
    "country": "country4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

