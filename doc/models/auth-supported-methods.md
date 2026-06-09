
# Auth Supported Methods

Metadata specifically related to which auth methods an institution supports.

*This model accepts additional fields of type unknown.*

## Structure

`AuthSupportedMethods`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `instantAuth` | `boolean` | Required | Indicates if instant auth is supported. |
| `instantMatch` | `boolean` | Required | Indicates if instant match is supported. |
| `automatedMicroDeposits` | `boolean` | Required | Indicates if automated microdeposits are supported. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "instant_auth": false,
  "instant_match": false,
  "automated_micro_deposits": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

