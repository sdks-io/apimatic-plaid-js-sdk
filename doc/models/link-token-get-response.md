
# Link Token Get Response

LinkTokenGetResponse defines the response schema for `/link/token/get`

## Structure

`LinkTokenGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `linkToken` | `string` | Required | A `link_token`, which can be supplied to Link in order to initialize it and receive a `public_token`, which can be exchanged for an `access_token`. |
| `createdAt` | `string \| null` | Required | The creation timestamp for the `link_token`, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format. |
| `expiration` | `string \| null` | Required | The expiration timestamp for the `link_token`, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format. |
| `metadata` | [`LinkTokenGetMetadataResponse`](../../doc/models/link-token-get-metadata-response.md) | Required | An object specifying the arguments originally provided to the `/link/token/create` call. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "link_token": "link_token0",
  "created_at": "2016-03-13T12:52:32.123Z",
  "expiration": "2016-03-13T12:52:32.123Z",
  "metadata": {
    "initial_products": [
      "transfer",
      "assets"
    ],
    "webhook": "webhook4",
    "country_codes": [
      "GB",
      "ES"
    ],
    "language": "language8",
    "account_filters": {
      "depository": {
        "account_subtypes": [
          "non-taxable brokerage account",
          "other"
        ]
      },
      "credit": {
        "account_subtypes": [
          "ugma",
          "utma",
          "variable annuity"
        ]
      },
      "loan": {
        "account_subtypes": [
          "checking",
          "savings",
          "money market"
        ]
      },
      "investment": {
        "account_subtypes": [
          "consumer",
          "home"
        ]
      }
    },
    "redirect_uri": "redirect_uri4",
    "client_name": "client_name0"
  },
  "request_id": "request_id6"
}
```

