
# Sandbox Processor Token Create Request Options

An optional set of options to be used when configuring the Item. If specified, must not be `null`.

## Structure

`SandboxProcessorTokenCreateRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `overrideUsername` | `string \| null \| undefined` | Optional | Test username to use for the creation of the Sandbox Item. Default value is `user_good`.<br><br>**Default**: `'user_good'` |
| `overridePassword` | `string \| null \| undefined` | Optional | Test password to use for the creation of the Sandbox Item. Default value is `pass_good`.<br><br>**Default**: `'pass_good'` |

## Example (as JSON)

```json
{
  "override_username": "user_good",
  "override_password": "pass_good"
}
```

