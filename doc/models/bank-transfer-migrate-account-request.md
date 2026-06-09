
# Bank Transfer Migrate Account Request

Defines the request schema for `/bank_transfer/migrate_account`

## Structure

`BankTransferMigrateAccountRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accountNumber` | `string` | Required | The user's account number. |
| `routingNumber` | `string` | Required | The user's routing number. |
| `accountType` | `string` | Required | The type of the bank account (`checking` or `savings`). |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "account_number": "account_number4",
  "routing_number": "routing_number8",
  "account_type": "account_type0"
}
```

