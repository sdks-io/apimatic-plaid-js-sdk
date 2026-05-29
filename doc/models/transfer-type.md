
# Transfer Type

Activity that modifies a position, but not through buy/sell activity e.g. options exercise, portfolio transfer

*This model accepts additional fields of type unknown.*

## Structure

`TransferType`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignment` | `string \| undefined` | Optional | Assignment of short option holding |
| `adjustment` | `string \| undefined` | Optional | Increase or decrease in quantity of item |
| `exercise` | `string \| undefined` | Optional | Exercise of an option or warrant contract |
| `expire` | `string \| undefined` | Optional | Expiration of an option or warrant contract |
| `merger` | `string \| undefined` | Optional | Stock exchanged at a pre-defined ratio as part of a merger between companies |
| `spinOff` | `string \| undefined` | Optional | Inflow of stock from spin-off transaction of an existing holding |
| `split` | `string \| undefined` | Optional | Inflow of stock from a forward split of an existing holding |
| `transfer` | `string \| undefined` | Optional | Movement of assets into or out of an account |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "assignment": "assignment8",
  "adjustment": "adjustment6",
  "exercise": "exercise4",
  "expire": "expire4",
  "merger": "merger2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

