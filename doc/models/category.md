
# Category

Information describing a transaction category

*This model accepts additional fields of type unknown.*

## Structure

`Category`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categoryId` | `string` | Required | An identifying number for the category. `category_id` is a Plaid-specific identifier and does not necessarily correspond to merchant category codes. |
| `group` | `string` | Required | `place` for physical transactions or `special` for other transactions such as bank charges. |
| `hierarchy` | `string[]` | Required | A hierarchical array of the categories to which this `category_id` belongs. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "category_id": "category_id0",
  "group": "group6",
  "hierarchy": [
    "hierarchy4",
    "hierarchy5"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

