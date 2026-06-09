
# Investments Transactions Get Request Options

An optional object to filter `/investments/transactions/get` results. If provided, must be non-`null`.

*This model accepts additional fields of type unknown.*

## Structure

`InvestmentsTransactionsGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | An array of `account_ids` to retrieve for the Item. |
| `count` | `number \| undefined` | Optional | The number of transactions to fetch.<br><br>**Default**: `100`<br><br>**Constraints**: `>= 1`, `<= 500` |
| `offset` | `number \| undefined` | Optional | The number of transactions to skip when fetching transaction history<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "count": 100,
  "offset": 0,
  "account_ids": [
    "account_ids7"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

