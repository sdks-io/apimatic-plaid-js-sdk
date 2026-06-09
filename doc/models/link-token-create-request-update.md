
# Link Token Create Request Update

Specifies options for initializing Link for [update mode](https://plaid.com/docs/link/update-mode).

## Structure

`LinkTokenCreateRequestUpdate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountSelectionEnabled` | `boolean \| undefined` | Optional | If `true`, enables [update mode with Account Select](https://plaid.com/docs/link/update-mode/#using-update-mode-to-request-new-accounts).<br><br>**Default**: `false` |

## Example (as JSON)

```json
{
  "account_selection_enabled": false
}
```

