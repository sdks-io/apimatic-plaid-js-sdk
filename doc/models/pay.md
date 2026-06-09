
# Pay

An object representing a monetary amount.

*This model accepts additional fields of type unknown.*

## Structure

`Pay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `number \| null \| undefined` | Optional | A numerical amount of a specific currency. |
| `currency` | `string \| null \| undefined` | Optional | Currency code, e.g. USD<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "amount": 242.24,
  "currency": "currency2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

