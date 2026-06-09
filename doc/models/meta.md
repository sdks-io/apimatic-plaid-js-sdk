
# Meta

Allows specifying the metadata of the test account

*This model accepts additional fields of type unknown.*

## Structure

`Meta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | The account's name |
| `officialName` | `string` | Required | The account's official name |
| `limit` | `number` | Required | The account's limit |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "name": "name8",
  "official_name": "official_name0",
  "limit": 109.44,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

