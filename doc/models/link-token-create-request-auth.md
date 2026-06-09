
# Link Token Create Request Auth

Specifies options for initializing Link for use with the Auth product. This field is currently only required if using the Flexible Auth product (currently in closed beta).

## Structure

`LinkTokenCreateRequestAuth`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `flowType` | `string` | Required | The optional Auth flow to use. Currently only used to enable Flexible Auth. |

## Example (as JSON)

```json
{
  "flow_type": "FLEXIBLE_AUTH"
}
```

