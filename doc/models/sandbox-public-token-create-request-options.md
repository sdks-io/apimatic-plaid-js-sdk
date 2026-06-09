
# Sandbox Public Token Create Request Options

An optional set of options to be used when configuring the Item. If specified, must not be `null`.

*This model accepts additional fields of type unknown.*

## Structure

`SandboxPublicTokenCreateRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook` | `string \| undefined` | Optional | Specify a webhook to associate with the new Item. |
| `overrideUsername` | `string \| null \| undefined` | Optional | Test username to use for the creation of the Sandbox Item. Default value is `user_good`.<br><br>**Default**: `'user_good'` |
| `overridePassword` | `string \| null \| undefined` | Optional | Test password to use for the creation of the Sandbox Item. Default value is `pass_good`.<br><br>**Default**: `'pass_good'` |
| `transactions` | [`SandboxPublicTokenCreateRequestOptionsTransactions \| undefined`](../../doc/models/sandbox-public-token-create-request-options-transactions.md) | Optional | SandboxPublicTokenCreateRequestOptionsTransactions is an optional set of parameters corresponding to transactions options. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "override_username": "user_good",
  "override_password": "pass_good",
  "webhook": "webhook8",
  "transactions": {
    "start_date": "2016-03-13T12:52:32.123Z",
    "end_date": "2016-03-13T12:52:32.123Z",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

