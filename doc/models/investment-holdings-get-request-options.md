
# Investment Holdings Get Request Options

An optional object to filter `/investments/holdings/get` results. If provided, must not be `null`.

*This model accepts additional fields of type unknown.*

## Structure

`InvestmentHoldingsGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | An array of `account_id`s to retrieve for the Item. An error will be returned if a provided `account_id` is not associated with the Item. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids7"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

