
# Bank Transfer User

The legal name and other information for the account holder.

*This model accepts additional fields of type unknown.*

## Structure

`BankTransferUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `legalName` | `string` | Required | The account holder’s full legal name. If the transfer description is `ccd`, this should be the business name of the account holder. |
| `emailAddress` | `string \| null \| undefined` | Optional | The account holder’s email. |
| `routingNumber` | `string \| undefined` | Optional | The account holder's routing number. This field is only used in response data. Do not provide this field when making requests. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "legal_name": "legal_name8",
  "email_address": "email_address8",
  "routing_number": "routing_number4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

