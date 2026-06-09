
# Connected Application

Describes the connected application for a particular end user.

## Structure

`ConnectedApplication`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationId` | `string` | Required | This field will map to the application ID that is returned from /item/applications/list, or provided to the institution in an oauth redirect. |
| `name` | `string` | Required | The name of the application |
| `logo` | `string \| null` | Required | A URL that links to the application logo image (will be deprecated in the future, please use logo_url). |
| `logoUrl` | `string \| null` | Required | A URL that links to the application logo image. |
| `applicationUrl` | `string \| null` | Required | The URL for the application's website |
| `reasonForAccess` | `string \| null` | Required | A string provided by the connected app stating why they use their respective enabled products. |
| `createdAt` | `string` | Required | The date this application was linked in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) (YYYY-MM-DD) format in UTC. |
| `productDataTypes` | [`ProductDataTypeEnum[]`](../../doc/models/product-data-type-enum.md) | Required | (Deprecated) A list of enums representing the data collected and products enabled for this connected application. |
| `scopes` | [`ScopesNullable \| undefined`](../../doc/models/scopes-nullable.md) | Optional | - |
| `requestedScopes` | [`RequestedScopes \| undefined`](../../doc/models/requested-scopes.md) | Optional | Scope of required and optional account features or content from a ConnectedApplication. |

## Example (as JSON)

```json
{
  "application_id": "application_id8",
  "name": "name2",
  "logo": "logo8",
  "logo_url": "logo_url2",
  "application_url": "application_url2",
  "reason_for_access": "reason_for_access0",
  "created_at": "2020-01-01",
  "product_data_types": [
    "ACCOUNT_BALANCE"
  ],
  "scopes": {
    "product_access": {
      "statements": false,
      "identity": false,
      "auth": false,
      "transactions": false
    },
    "accounts": [
      {
        "unique_id": "unique_id6",
        "authorized": false
      },
      {
        "unique_id": "unique_id6",
        "authorized": false
      }
    ],
    "new_accounts": false
  },
  "requested_scopes": {
    "required_product_access": {
      "statements": false,
      "identity": false,
      "auth": false,
      "transactions": false
    },
    "optional_product_access": {
      "statements": false,
      "identity": false,
      "auth": false,
      "transactions": false
    },
    "account_filters": {
      "depository": [
        "depository1",
        "depository2"
      ],
      "credit": [
        "credit2"
      ],
      "loan": [
        "loan9"
      ],
      "investment": [
        "investment1",
        "investment2",
        "investment3"
      ]
    },
    "account_selection_cardinality": "MULTI_SELECT"
  }
}
```

