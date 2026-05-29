
# Sandbox Oauth Select Accounts Request

Defines the request schema for `sandbox/oauth/select_accounts`

*This model accepts additional fields of type unknown.*

## Structure

`SandboxOauthSelectAccountsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `oauthStateId` | `string` | Required | - |
| `accounts` | `string[]` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "oauth_state_id": "oauth_state_id6",
  "accounts": [
    "accounts2"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

