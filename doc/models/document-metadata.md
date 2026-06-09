
# Document Metadata

An object representing metadata from the end user's uploaded document.

## Structure

`DocumentMetadata`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The name of the document. |
| `status` | `string \| undefined` | Optional | The processing status of the document. |
| `docId` | `string \| undefined` | Optional | An identifier of the document that is also present in the paystub response. |

## Example (as JSON)

```json
{
  "name": "name4",
  "status": "status6",
  "doc_id": "doc_id8"
}
```

