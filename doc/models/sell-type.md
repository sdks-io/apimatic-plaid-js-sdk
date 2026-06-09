
# Sell Type

Selling an investment

*This model accepts additional fields of type unknown.*

## Structure

`SellType`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distribution` | `string \| undefined` | Optional | Outflow of assets from a tax-advantaged account |
| `exercise` | `string \| undefined` | Optional | Exercise of an option or warrant contract |
| `sell` | `string \| undefined` | Optional | Sell to close or decrease an existing holding |
| `sellShort` | `string \| undefined` | Optional | Sell to open a short position |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "distribution": "distribution8",
  "exercise": "exercise0",
  "sell": "sell0",
  "sell short": "sell short0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

