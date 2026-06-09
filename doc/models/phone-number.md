
# Phone Number

A phone number

## Structure

`PhoneNumber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `string` | Required | The phone number. |
| `primary` | `boolean` | Required | When `true`, identifies the phone number as the primary number on an account. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | The type of phone number. |

## Example (as JSON)

```json
{
  "data": "data2",
  "primary": false,
  "type": "home"
}
```

