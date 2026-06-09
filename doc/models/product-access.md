
# Product Access

The product access being requested. Used to or disallow product access across all accounts. If unset, defaults to all products allowed.

## Structure

`ProductAccess`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statements` | `boolean \| null \| undefined` | Optional | Allow access to statements. If unset, defaults to `true`.<br><br>**Default**: `true` |
| `identity` | `boolean \| null \| undefined` | Optional | Allow access to the Identity product (name, email, phone, address). If unset, defaults to `true`.<br><br>**Default**: `true` |
| `auth` | `boolean \| null \| undefined` | Optional | Allow access to account number details. If unset, defaults to `true`.<br><br>**Default**: `true` |
| `transactions` | `boolean \| null \| undefined` | Optional | Allow access to transaction details. If unset, defaults to `true`.<br><br>**Default**: `true` |

## Example (as JSON)

```json
{
  "statements": true,
  "identity": true,
  "auth": true,
  "transactions": true
}
```

