
# Paystub Ytd Details

The amount of income earned year to date, as based on paystub data.

*This model accepts additional fields of type unknown.*

## Structure

`PaystubYtdDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `grossEarnings` | `number \| null \| undefined` | Optional | Year-to-date gross earnings. |
| `netEarnings` | `number \| null \| undefined` | Optional | Year-to-date net (take home) earnings. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "gross_earnings": 11.24,
  "net_earnings": 55.46,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

