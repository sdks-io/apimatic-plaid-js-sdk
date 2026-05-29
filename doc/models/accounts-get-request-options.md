
# Accounts Get Request Options

An optional object to filter `/accounts/get` results.

*This model accepts additional fields of type unknown.*

## Structure

`AccountsGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | An array of `account_ids` to retrieve for the Account. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_ids": [
    "account_ids7",
    "account_ids8",
    "account_ids9"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

