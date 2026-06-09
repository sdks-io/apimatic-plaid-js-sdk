
# Employers Search Request

EmployersSearchRequest defines the request schema for `/employers/search`.

## Structure

`EmployersSearchRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `query` | `string` | Required | The employer name to be searched for. |
| `products` | `string[]` | Required | The Plaid products the returned employers should support. Currently, this field must be set to `"deposit_switch"`. |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "query": "query4",
  "products": [
    "products2",
    "products3",
    "products4"
  ]
}
```

