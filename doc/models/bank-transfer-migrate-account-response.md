
# Bank Transfer Migrate Account Response

Defines the response schema for `/bank_transfer/migrate_account`

## Structure

`BankTransferMigrateAccountResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | The Plaid `access_token` for the newly created Item. |
| `accountId` | `string` | Required | The Plaid `account_id` for the newly created Item. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "access_token": "access_token4",
  "account_id": "account_id8",
  "request_id": "request_id2"
}
```

