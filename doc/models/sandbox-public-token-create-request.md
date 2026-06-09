
# Sandbox Public Token Create Request

SandboxPublicTokenCreateRequest defines the request schema for `/sandbox/public_token/create`

## Structure

`SandboxPublicTokenCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `institutionId` | `string` | Required | The ID of the institution the Item will be associated with |
| `initialProducts` | [`ProductsEnum[]`](../../doc/models/products-enum.md) | Required | The products to initially pull for the Item. May be any products that the specified `institution_id`  supports. This array may not be empty.<br><br>**Constraints**: *Minimum Items*: `1` |
| `options` | [`SandboxPublicTokenCreateRequestOptions \| undefined`](../../doc/models/sandbox-public-token-create-request-options.md) | Optional | An optional set of options to be used when configuring the Item. If specified, must not be `null`. |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "secret": "secret4",
  "institution_id": "institution_id6",
  "initial_products": [
    "auth",
    "balance"
  ],
  "options": {
    "webhook": "webhook0",
    "override_username": "override_username0",
    "override_password": "override_password8",
    "transactions": {
      "start_date": "2016-03-13T12:52:32.123Z",
      "end_date": "2016-03-13T12:52:32.123Z"
    }
  }
}
```

