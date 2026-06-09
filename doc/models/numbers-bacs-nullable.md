
# Numbers BACS Nullable

## Structure

`NumbersBACSNullable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `account` | `string` | Required | The BACS account number for the account |
| `sortCode` | `string` | Required | The BACS sort code for the account |

## Example (as JSON)

```json
{
  "account_id": "account_id8",
  "account": "account6",
  "sort_code": "sort_code6"
}
```

