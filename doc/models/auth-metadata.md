
# Auth Metadata

Metadata that captures information about the Auth features of an institution.

*This model accepts additional fields of type unknown.*

## Structure

`AuthMetadata`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `supportedMethods` | [`AuthSupportedMethods`](../../doc/models/auth-supported-methods.md) | Required | Metadata specifically related to which auth methods an institution supports. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "supported_methods": {
    "instant_auth": false,
    "instant_match": false,
    "automated_micro_deposits": false,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

