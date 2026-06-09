
# Item Application List Response

Describes the connected application for a particular end user.

## Structure

`ItemApplicationListResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string \| undefined` | Optional | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `applications` | [`ConnectedApplication[]`](../../doc/models/connected-application.md) | Required | A list of connected applications. |

## Example (as JSON)

```json
{
  "applications": [
    {
      "application_id": "application_id6",
      "name": "name8",
      "logo": "logo6",
      "logo_url": "logo_url2",
      "application_url": "application_url2",
      "reason_for_access": "reason_for_access6",
      "created_at": "2020-01-01",
      "product_data_types": [
        "ACCOUNT_TRANSACTIONS",
        "ACCOUNT_BALANCE",
        "ACCOUNT_USER_INFO"
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
  ],
  "request_id": "request_id4"
}
```

