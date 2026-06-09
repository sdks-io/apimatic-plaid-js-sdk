
# Identity Get Request Options

An optional object to filter `/identity/get` results.

## Structure

`IdentityGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | A list of `account_ids` to retrieve for the Item.<br>Note: An error will be returned if a provided `account_id` is not associated with the Item. |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids3",
    "account_ids4",
    "account_ids5"
  ]
}
```

