
# Link Token Eu Config

Configuration parameters for EU flows

*This model accepts additional fields of type unknown.*

## Structure

`LinkTokenEuConfig`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `headless` | `boolean \| undefined` | Optional | If `true`, open Link without an initial UI. Defaults to `false`. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "headless": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

