
# Requested Scopes

Scope of required and optional account features or content from a ConnectedApplication.

## Structure

`RequestedScopes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requiredProductAccess` | [`ProductAccess`](../../doc/models/product-access.md) | Required | The product access being requested. Used to or disallow product access across all accounts. If unset, defaults to all products allowed. |
| `optionalProductAccess` | [`ProductAccess`](../../doc/models/product-access.md) | Required | The product access being requested. Used to or disallow product access across all accounts. If unset, defaults to all products allowed. |
| `accountFilters` | [`AccountFilter \| undefined`](../../doc/models/account-filter.md) | Optional | Enumerates the account subtypes that the application wishes for the user to be able to select from. For more details refer to Plaid documentation on account filters. |
| `accountSelectionCardinality` | [`AccountSelectionCardinalityEnum`](../../doc/models/account-selection-cardinality-enum.md) | Required | The application requires that accounts be limited to a specific cardinality.<br>`MULTI_SELECT`: indicates that the user should be allowed to pick multiple accounts.<br>`SINGLE_SELECT`: indicates that the user should be allowed to pick only a single account.<br>`ALL`: indicates that the user must share all of their accounts and should not be given the opportunity to de-select |

## Example (as JSON)

```json
{
  "required_product_access": {
    "statements": true,
    "identity": true,
    "auth": true,
    "transactions": true
  },
  "optional_product_access": {
    "statements": true,
    "identity": true,
    "auth": true,
    "transactions": true
  },
  "account_selection_cardinality": "ALL",
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
  }
}
```

