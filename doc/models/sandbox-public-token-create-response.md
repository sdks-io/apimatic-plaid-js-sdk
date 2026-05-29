
# Sandbox Public Token Create Response

SandboxPublicTokenCreateResponse defines the response schema for `/sandbox/public_token/create`

*This model accepts additional fields of type unknown.*

## Structure

`SandboxPublicTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `publicToken` | `string` | Required | A public token that can be exchanged for an access token using `/item/public_token/exchange` |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "public_token": "public_token4",
  "request_id": "request_id6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

