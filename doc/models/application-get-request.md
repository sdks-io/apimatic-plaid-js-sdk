
# Application Get Request

ApplicationGetResponse defines the schema for `/application/get`

## Structure

`ApplicationGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string` | Required | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string` | Required | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `applicationId` | `string` | Required | This field will map to the application ID that is returned from /item/applications/list, or provided to the institution in an oauth redirect. |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret2",
  "application_id": "application_id2"
}
```

