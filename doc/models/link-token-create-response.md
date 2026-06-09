
# Link Token Create Response

LinkTokenCreateResponse defines the response schema for `/link/token/create`

## Structure

`LinkTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `linkToken` | `string` | Required | A `link_token`, which can be supplied to Link in order to initialize it and receive a `public_token`, which can be exchanged for an `access_token`. |
| `expiration` | `string` | Required | The expiration date for the `link_token`, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format. A `link_token` created to generate a `public_token` that will be exchanged for a new `access_token` expires after 4 hours. A `link_token` created for an existing Item (such as when updating an existing `access_token` by launching Link in update mode) expires after 30 minutes. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "link_token": "link_token0",
  "expiration": "2016-03-13T12:52:32.123Z",
  "request_id": "request_id6"
}
```

