
# Pay

An object representing a monetary amount.

## Structure

`Pay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `number \| null \| undefined` | Optional | A numerical amount of a specific currency. |
| `currency` | `string \| null \| undefined` | Optional | Currency code, e.g. USD<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |

## Example (as JSON)

```json
{
  "amount": 242.24,
  "currency": "currency2"
}
```

