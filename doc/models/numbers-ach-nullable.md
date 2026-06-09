
# Numbers ACH Nullable

## Structure

`NumbersACHNullable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `account` | `string` | Required | The ACH account number for the account.<br><br>Note that when using OAuth with Chase Bank (`ins_56`), Chase will issue "tokenized" routing and account numbers, which are not the user's actual account and routing numbers. These tokenized numbers should work identically to normal account and routing numbers. The digits returned in the mask field will continue to reflect the actual account number, rather than the tokenized account number. If a user revokes their permissions to your app, the tokenized numbers will continue to work for ACH deposits, but not withdrawals. |
| `routing` | `string` | Required | The ACH routing number for the account. If the institution is `ins_56`, this may be a tokenized routing number. For more information, see the description of the `account` field. |
| `wireRouting` | `string \| null` | Required | The wire transfer routing number for the account, if available |

## Example (as JSON)

```json
{
  "account_id": "account_id8",
  "account": "account6",
  "routing": "routing2",
  "wire_routing": "wire_routing6"
}
```

