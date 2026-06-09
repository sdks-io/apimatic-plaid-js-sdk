
# Item Application List User Auth

User authentication parameters, for clients making a request without an `access_token`. This is only allowed for select clients and will not be supported in the future. Most clients should call /item/import to obtain an access token before making a request.

## Structure

`ItemApplicationListUserAuth`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `userId` | `string \| null \| undefined` | Optional | Account username. |
| `fiUsernameHash` | `string \| null \| undefined` | Optional | Account username hashed by FI. |

## Example (as JSON)

```json
{
  "user_id": "user_id4",
  "fi_username_hash": "fi_username_hash2"
}
```

