
# Email

An object representing an email address

## Structure

`Email`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `string` | Required | The email address. |
| `primary` | `boolean` | Required | When `true`, identifies the email address as the primary email on an account. |
| `type` | [`Type1Enum`](../../doc/models/type-1-enum.md) | Required | The type of email account as described by the financial institution. |

## Example (as JSON)

```json
{
  "data": "data4",
  "primary": false,
  "type": "other"
}
```

