
# Item Import Request Options

An optional object to configure `/item/import` request.

*This model accepts additional fields of type unknown.*

## Structure

`ItemImportRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook` | `string \| undefined` | Optional | Specifies a webhook URL to associate with an Item. Plaid fires a webhook if credentials fail. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "webhook": "webhook4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

