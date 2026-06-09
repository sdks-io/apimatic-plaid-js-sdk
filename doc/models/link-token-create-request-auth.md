
# Link Token Create Request Auth

Specifies options for initializing Link for use with the Auth product. This field is currently only required if using the Flexible Auth product (currently in closed beta).

*This model accepts additional fields of type unknown.*

## Structure

`LinkTokenCreateRequestAuth`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `flowType` | `string` | Required | The optional Auth flow to use. Currently only used to enable Flexible Auth. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "flow_type": "FLEXIBLE_AUTH",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

