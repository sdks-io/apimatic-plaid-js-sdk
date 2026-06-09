
# Liabilities Get Request Options

An optional object to filter `/liabilities/get` results. If provided, `options` cannot be null.

## Structure

`LiabilitiesGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | A list of accounts to retrieve for the Item.<br><br>An error will be returned if a provided `account_id` is not associated with the Item |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids9",
    "account_ids0"
  ]
}
```

