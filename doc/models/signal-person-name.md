
# Signal Person Name

The user's legal name

*This model accepts additional fields of type unknown.*

## Structure

`SignalPersonName`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prefix` | `string \| null \| undefined` | Optional | The user's name prefix (e.g. "Mr.") |
| `givenName` | `string \| null \| undefined` | Optional | The user's given name. If the user has a one-word name, it should be provided in this field. |
| `middleName` | `string \| null \| undefined` | Optional | The user's middle name |
| `familyName` | `string \| null \| undefined` | Optional | The user's family name / surname |
| `suffix` | `string \| null \| undefined` | Optional | The user's name suffix (e.g. "II") |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "prefix": "prefix6",
  "given_name": "given_name0",
  "middle_name": "middle_name8",
  "family_name": "family_name2",
  "suffix": "suffix8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

