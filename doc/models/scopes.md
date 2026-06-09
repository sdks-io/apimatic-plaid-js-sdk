
# Scopes

The scopes object

## Structure

`Scopes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `productAccess` | [`ProductAccess \| undefined`](../../doc/models/product-access.md) | Optional | The product access being requested. Used to or disallow product access across all accounts. If unset, defaults to all products allowed. |
| `accounts` | [`AccountAccess[] \| undefined`](../../doc/models/account-access.md) | Optional | - |
| `newAccounts` | `boolean \| null \| undefined` | Optional | Allow access to newly opened accounts as they are opened. If unset, defaults to `true`.<br><br>**Default**: `true` |

## Example (as JSON)

```json
{
  "new_accounts": true,
  "product_access": {
    "statements": false,
    "identity": false,
    "auth": false,
    "transactions": false
  },
  "accounts": [
    {
      "unique_id": "unique_id6",
      "authorized": false
    },
    {
      "unique_id": "unique_id6",
      "authorized": false
    }
  ]
}
```

