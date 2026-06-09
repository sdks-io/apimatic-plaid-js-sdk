
# Document Metadata

An object representing metadata from the end user's uploaded document.

*This model accepts additional fields of type unknown.*

## Structure

`DocumentMetadata`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The name of the document. |
| `status` | `string \| undefined` | Optional | The processing status of the document. |
| `docId` | `string \| undefined` | Optional | An identifier of the document that is also present in the paystub response. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "name": "name4",
  "status": "status6",
  "doc_id": "doc_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

