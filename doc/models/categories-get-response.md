
# Categories Get Response

CategoriesGetResponse defines the response schema for `/categories/get`

## Structure

`CategoriesGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categories` | [`Category[]`](../../doc/models/category.md) | Required | An array of all of the transaction categories used by Plaid. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "categories": [
    {
      "category_id": "category_id0",
      "group": "group6",
      "hierarchy": [
        "hierarchy4"
      ]
    }
  ],
  "request_id": "request_id2"
}
```

