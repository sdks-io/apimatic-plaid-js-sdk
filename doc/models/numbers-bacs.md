
# Numbers Bacs

Identifying information for transferring money to or from a UK bank account via BACS.

*This model accepts additional fields of type unknown.*

## Structure

`NumbersBacs`

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
  "account_id": "account_id6",
  "account": "account4",
  "sort_code": "sort_code4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

