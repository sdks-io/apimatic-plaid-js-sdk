
# Auth Metadata

Metadata that captures information about the Auth features of an institution.

## Structure

`AuthMetadata`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `supportedMethods` | [`AuthSupportedMethods`](../../doc/models/auth-supported-methods.md) | Required | Metadata specifically related to which auth methods an institution supports. |

## Example (as JSON)

```json
{
  "supported_methods": {
    "instant_auth": false,
    "instant_match": false,
    "automated_micro_deposits": false
  }
}
```

