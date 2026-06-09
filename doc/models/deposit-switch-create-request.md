
# Deposit Switch Create Request

DepositSwitchCreateRequest defines the request schema for `/deposit_switch/create`

## Structure

`DepositSwitchCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `targetAccessToken` | `string` | Required | Access token for the target Item, typically provided in the Import Item response. |
| `targetAccountId` | `string` | Required | Plaid Account ID that specifies the target bank account. This account will become the recipient for a user's direct deposit. |
| `countryCode` | [`CountryCode1Enum \| undefined`](../../doc/models/country-code-1-enum.md) | Optional | ISO-3166-1 alpha-2 country code standard. |
| `options` | [`DepositSwitchCreateRequestOptions \| undefined`](../../doc/models/deposit-switch-create-request-options.md) | Optional | Options to configure the `/deposit_switch/create` request. If provided, cannot be `null`. |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "target_access_token": "target_access_token2",
  "target_account_id": "target_account_id6",
  "country_code": "US",
  "options": {
    "webhook": "webhook0",
    "transaction_item_access_tokens": [
      "transaction_item_access_tokens4",
      "transaction_item_access_tokens5",
      "transaction_item_access_tokens6"
    ]
  }
}
```

