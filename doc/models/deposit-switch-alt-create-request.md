
# Deposit Switch Alt Create Request

DepositSwitchAltCreateRequest defines the request schema for `/deposit_switch/alt/create`

## Structure

`DepositSwitchAltCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `targetAccount` | [`DepositSwitchTargetAccount`](../../doc/models/deposit-switch-target-account.md) | Required | - |
| `targetUser` | [`DepositSwitchTargetUser`](../../doc/models/deposit-switch-target-user.md) | Required | - |
| `options` | [`DepositSwitchCreateRequestOptions \| undefined`](../../doc/models/deposit-switch-create-request-options.md) | Optional | Options to configure the `/deposit_switch/create` request. If provided, cannot be `null`. |
| `countryCode` | [`CountryCode1Enum \| undefined`](../../doc/models/country-code-1-enum.md) | Optional | ISO-3166-1 alpha-2 country code standard. |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret8",
  "target_account": {
    "account_number": "account_number8",
    "routing_number": "routing_number6",
    "account_name": "account_name0",
    "account_subtype": "checking"
  },
  "target_user": {
    "given_name": "given_name6",
    "family_name": "family_name8",
    "phone": "phone4",
    "email": "email2",
    "address": {
      "city": "city6",
      "region": "region2",
      "street": "street6",
      "postal_code": "postal_code8",
      "country": "country0"
    },
    "tax_payer_id": "tax_payer_id2"
  },
  "options": {
    "webhook": "webhook0",
    "transaction_item_access_tokens": [
      "transaction_item_access_tokens4",
      "transaction_item_access_tokens5",
      "transaction_item_access_tokens6"
    ]
  },
  "country_code": "US"
}
```

