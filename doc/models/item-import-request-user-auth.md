
# Item Import Request User Auth

Object of user ID and auth token pair, permitting Plaid to aggregate a user’s accounts

*This model accepts additional fields of type unknown.*

## Structure

`ItemImportRequestUserAuth`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `userId` | `string` | Required | Opaque user identifier |
| `authToken` | `string` | Required | Authorization token Plaid will use to aggregate this user’s accounts |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "user_id": "user_id2",
  "auth_token": "auth_token0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

