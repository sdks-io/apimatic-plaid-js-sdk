
# Auth Get Request

AuthGetRequest defines the request schema for `/auth/get`

*This model accepts additional fields of type unknown.*

## Structure

`AuthGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `options` | [`AuthGetRequestOptions \| undefined`](../../doc/models/auth-get-request-options.md) | Optional | An optional object to filter `/auth/get` results. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "access_token": "access_token4",
  "options": {
    "account_ids": [
      "account_ids3",
      "account_ids4",
      "account_ids5"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

