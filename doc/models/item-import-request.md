
# Item Import Request

ItemImportRequest defines the request schema for `/item/import`

## Structure

`ItemImportRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `products` | [`ProductsEnum[]`](../../doc/models/products-enum.md) | Required | Array of product strings<br><br>**Constraints**: *Minimum Items*: `1` |
| `userAuth` | [`ItemImportRequestUserAuth`](../../doc/models/item-import-request-user-auth.md) | Required | Object of user ID and auth token pair, permitting Plaid to aggregate a user’s accounts |
| `options` | [`ItemImportRequestOptions \| undefined`](../../doc/models/item-import-request-options.md) | Optional | An optional object to configure `/item/import` request. |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "secret": "secret4",
  "products": [
    "investments",
    "liabilities",
    "payment_initiation"
  ],
  "user_auth": {
    "user_id": "user_id2",
    "auth_token": "auth_token0"
  },
  "options": {
    "webhook": "webhook0"
  }
}
```

