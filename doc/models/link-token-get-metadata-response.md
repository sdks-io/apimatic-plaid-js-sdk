
# Link Token Get Metadata Response

An object specifying the arguments originally provided to the `/link/token/create` call.

## Structure

`LinkTokenGetMetadataResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `initialProducts` | [`ProductsEnum[]`](../../doc/models/products-enum.md) | Required | The `products` specified in the `/link/token/create` call. |
| `webhook` | `string \| null` | Required | The `webhook` specified in the `/link/token/create` call. |
| `countryCodes` | [`CountryCodeEnum[]`](../../doc/models/country-code-enum.md) | Required | The `country_codes` specified in the `/link/token/create` call. |
| `language` | `string \| null` | Required | The `language` specified in the `/link/token/create` call. |
| `accountFilters` | [`AccountFiltersResponse \| undefined`](../../doc/models/account-filters-response.md) | Optional | The `account_filters` specified in the original call to `/link/token/create`. |
| `redirectUri` | `string \| null` | Required | The `redirect_uri` specified in the `/link/token/create` call. |
| `clientName` | `string \| null` | Required | The `client_name` specified in the `/link/token/create` call. |

## Example (as JSON)

```json
{
  "initial_products": [
    "liabilities",
    "payment_initiation",
    "transactions"
  ],
  "webhook": "webhook4",
  "country_codes": [
    "US",
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
}
```

