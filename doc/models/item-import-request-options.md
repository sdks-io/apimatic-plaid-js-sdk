
# Item Import Request Options

An optional object to configure `/item/import` request.

## Structure

`ItemImportRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook` | `string \| undefined` | Optional | Specifies a webhook URL to associate with an Item. Plaid fires a webhook if credentials fail. |

## Example (as JSON)

```json
{
  "webhook": "webhook4"
}
```

