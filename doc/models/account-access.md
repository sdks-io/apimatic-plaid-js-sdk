
# Account Access

Allow or disallow product access by account. Unlisted (e.g. missing) accounts will be considered `new_accounts`.

## Structure

`AccountAccess`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uniqueId` | `string` | Required | The unique account identifier for this account. This value must match that returned by the data access API for this account. |
| `authorized` | `boolean \| null \| undefined` | Optional | Allow the application to see this account (and associated details, including balance) in the list of accounts. If unset, defaults to `true`.<br><br>**Default**: `true` |

## Example (as JSON)

```json
{
  "unique_id": "unique_id6",
  "authorized": true
}
```

