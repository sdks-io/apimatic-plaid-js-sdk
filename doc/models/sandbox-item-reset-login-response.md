
# Sandbox Item Reset Login Response

SandboxItemResetLoginResponse defines the response schema for `/sandbox/item/reset_login`

*This model accepts additional fields of type unknown.*

## Structure

`SandboxItemResetLoginResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resetLogin` | `boolean` | Required | `true` if the call succeeded |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "reset_login": false,
  "request_id": "request_id4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

