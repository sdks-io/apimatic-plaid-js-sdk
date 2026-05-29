
# Link Token Get Request

LinkTokenGetRequest defines the request schema for `/link/token/get`

*This model accepts additional fields of type unknown.*

## Structure

`LinkTokenGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `linkToken` | `string` | Required | A `link_token` from a previous invocation of `/link/token/create` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "secret": "secret6",
  "link_token": "link_token8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

