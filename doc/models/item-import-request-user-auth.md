
# Item Import Request User Auth

Object of user ID and auth token pair, permitting Plaid to aggregate a user’s accounts

## Structure

`ItemImportRequestUserAuth`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `userId` | `string` | Required | Opaque user identifier |
| `authToken` | `string` | Required | Authorization token Plaid will use to aggregate this user’s accounts |

## Example (as JSON)

```json
{
  "user_id": "user_id2",
  "auth_token": "auth_token0"
}
```

