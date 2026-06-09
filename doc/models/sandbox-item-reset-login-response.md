
# Sandbox Item Reset Login Response

SandboxItemResetLoginResponse defines the response schema for `/sandbox/item/reset_login`

## Structure

`SandboxItemResetLoginResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resetLogin` | `boolean` | Required | `true` if the call succeeded |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "reset_login": false,
  "request_id": "request_id4"
}
```

