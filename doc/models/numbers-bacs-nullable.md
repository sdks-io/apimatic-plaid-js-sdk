
# Numbers Bacs Nullable

*This model accepts additional fields of type unknown.*

## Structure

`NumbersBacsNullable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `account` | `string` | Required | The BACS account number for the account |
| `sortCode` | `string` | Required | The BACS sort code for the account |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_id": "account_id8",
  "account": "account6",
  "sort_code": "sort_code6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

