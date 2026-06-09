
# Investment Holdings Get Request Options

An optional object to filter `/investments/holdings/get` results. If provided, must not be `null`.

## Structure

`InvestmentHoldingsGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | An array of `account_id`s to retrieve for the Item. An error will be returned if a provided `account_id` is not associated with the Item. |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids7"
  ]
}
```

