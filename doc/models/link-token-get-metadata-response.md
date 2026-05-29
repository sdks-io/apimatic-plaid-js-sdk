
# Link Token Get Metadata Response

An object specifying the arguments originally provided to the `/link/token/create` call.

*This model accepts additional fields of type unknown.*

## Structure

`LinkTokenGetMetadataResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `initialProducts` | [`Products[]`](../../doc/models/products.md) | Required | The `products` specified in the `/link/token/create` call. |
| `webhook` | `string \| null` | Required | The `webhook` specified in the `/link/token/create` call. |
| `countryCodes` | [`CountryCode[]`](../../doc/models/country-code.md) | Required | The `country_codes` specified in the `/link/token/create` call. |
| `language` | `string \| null` | Required | The `language` specified in the `/link/token/create` call. |
| `accountFilters` | [`AccountFiltersResponse \| undefined`](../../doc/models/account-filters-response.md) | Optional | The `account_filters` specified in the original call to `/link/token/create`. |
| `redirectUri` | `string \| null` | Required | The `redirect_uri` specified in the `/link/token/create` call. |
| `clientName` | `string \| null` | Required | The `client_name` specified in the `/link/token/create` call. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

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
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "credit": {
      "account_subtypes": [
        "ugma",
        "utma",
        "variable annuity"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "loan": {
      "account_subtypes": [
        "checking",
        "savings",
        "money market"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "investment": {
      "account_subtypes": [
        "consumer",
        "home"
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
  },
  "redirect_uri": "redirect_uri4",
  "client_name": "client_name0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

