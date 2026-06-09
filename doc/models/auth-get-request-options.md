
# Auth Get Request Options

An optional object to filter `/auth/get` results.

## Structure

`AuthGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | A list of `account_ids` to retrieve for the Item.<br>Note: An error will be returned if a provided `account_id` is not associated with the Item. |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids7",
    "account_ids8"
  ]
}
```

