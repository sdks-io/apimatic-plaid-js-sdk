
# Categories Get Response

CategoriesGetResponse defines the response schema for `/categories/get`

*This model accepts additional fields of type unknown.*

## Structure

`CategoriesGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categories` | [`Category[]`](../../doc/models/category.md) | Required | An array of all of the transaction categories used by Plaid. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "categories": [
    {
      "category_id": "category_id0",
      "group": "group6",
      "hierarchy": [
        "hierarchy4"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

