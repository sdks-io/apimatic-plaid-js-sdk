
# Bank Transfer Balance Get Request

Defines the request schema for `/bank_transfer/balance/get`

## Structure

`BankTransferBalanceGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `originationAccountId` | `string \| null \| undefined` | Optional | If multiple origination accounts are available, `origination_account_id` must be used to specify the account for which balance will be returned. |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "secret": "secret4",
  "origination_account_id": "origination_account_id0"
}
```

