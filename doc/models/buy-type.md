
# Buy Type

Buying an investment

## Structure

`BuyType`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignment` | `string \| undefined` | Optional | Assignment of short option holding |
| `contribution` | `string \| undefined` | Optional | Inflow of assets into a tax-advantaged account |
| `buy` | `string \| undefined` | Optional | Purchase to open or increase a position |
| `buyToCover` | `string \| undefined` | Optional | Purchase to close a short position |
| `dividendReinvestment` | `string \| undefined` | Optional | Purchase using proceeds from a cash dividend |
| `interestReinvestment` | `string \| undefined` | Optional | Purchase using proceeds from a cash interest payment |
| `longTermCapitalGainReinvestment` | `string \| undefined` | Optional | Purchase using long-term capital gain cash proceeds |
| `shortTermCapitalGainReinvestment` | `string \| undefined` | Optional | Purchase using short-term capital gain cash proceeds |

## Example (as JSON)

```json
{
  "assignment": "assignment8",
  "contribution": "contribution2",
  "buy": "buy6",
  "buy to cover": "buy to cover8",
  "dividend reinvestment": "dividend reinvestment2"
}
```

