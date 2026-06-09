
# Phone Number

A phone number

*This model accepts additional fields of type unknown.*

## Structure

`PhoneNumber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `string` | Required | The phone number. |
| `primary` | `boolean` | Required | When `true`, identifies the phone number as the primary number on an account. |
| `type` | [`Type`](../../doc/models/type.md) | Required | The type of phone number. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "data": "data2",
  "primary": false,
  "type": "home",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

