
# Sandbox Oauth Select Accounts Request

Defines the request schema for `sandbox/oauth/select_accounts`

## Structure

`SandboxOauthSelectAccountsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `oauthStateId` | `string` | Required | - |
| `accounts` | `string[]` | Required | - |

## Example (as JSON)

```json
{
  "oauth_state_id": "oauth_state_id6",
  "accounts": [
    "accounts2"
  ]
}
```

