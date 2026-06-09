
# Unofficial Currency Code List

List of unofficial currency codes

*This model accepts additional fields of type unknown.*

## Structure

`UnofficialCurrencyCodeList`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ada` | `string` | Required | Cardano |
| `bat` | `string` | Required | Basic Attention Token |
| `bch` | `string` | Required | Bitcoin Cash |
| `bnb` | `string` | Required | Binance Coin |
| `btc` | `string` | Required | Bitcoin |
| `btg` | `string` | Required | Bitcoin Gold |
| `cnh` | `string` | Required | Chinese Yuan (offshore) |
| `dash` | `string` | Required | Dash |
| `doge` | `string` | Required | Dogecoin |
| `etc` | `string` | Required | Ethereum Classic |
| `eth` | `string` | Required | Ethereum |
| `gbx` | `string` | Required | Pence sterling, i.e. British penny |
| `lsk` | `string` | Required | Lisk |
| `neo` | `string` | Required | Neo |
| `omg` | `string` | Required | OmiseGO |
| `qtum` | `string` | Required | Qtum |
| `usdt` | `string` | Required | TehterUS |
| `xlm` | `string` | Required | Stellar Lumen |
| `xmr` | `string` | Required | Monero |
| `xrp` | `string` | Required | Ripple |
| `zec` | `string` | Required | Zcash |
| `zrx` | `string` | Required | 0x |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "ADA": "ADA4",
  "BAT": "BAT8",
  "BCH": "BCH8",
  "BNB": "BNB4",
  "BTC": "BTC0",
  "BTG": "BTG6",
  "CNH": "CNH6",
  "DASH": "DASH4",
  "DOGE": "DOGE4",
  "ETC": "ETC0",
  "ETH": "ETH6",
  "GBX": "GBX8",
  "LSK": "LSK4",
  "NEO": "NEO8",
  "OMG": "OMG6",
  "QTUM": "QTUM8",
  "USDT": "USDT8",
  "XLM": "XLM2",
  "XMR": "XMR0",
  "XRP": "XRP0",
  "ZEC": "ZEC4",
  "ZRX": "ZRX8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

