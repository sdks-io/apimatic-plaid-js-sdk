
# Category

Information describing a transaction category

## Structure

`Category`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categoryId` | `string` | Required | An identifying number for the category. `category_id` is a Plaid-specific identifier and does not necessarily correspond to merchant category codes. |
| `group` | `string` | Required | `place` for physical transactions or `special` for other transactions such as bank charges. |
| `hierarchy` | `string[]` | Required | A hierarchical array of the categories to which this `category_id` belongs. |

## Example (as JSON)

```json
{
  "category_id": "category_id0",
  "group": "group6",
  "hierarchy": [
    "hierarchy4",
    "hierarchy5"
  ]
}
```

