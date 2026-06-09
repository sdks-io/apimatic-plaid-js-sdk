
# Cash Type

Activity that modifies a cash position

*This model accepts additional fields of type unknown.*

## Structure

`CashType`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountFee` | `string \| undefined` | Optional | Fees paid for account maintenance |
| `contribution` | `string \| undefined` | Optional | Inflow of assets into a tax-advantaged account |
| `deposit` | `string \| undefined` | Optional | Inflow of cash into an account |
| `dividend` | `string \| undefined` | Optional | Inflow of cash from a dividend |
| `stockDistribution` | `string \| undefined` | Optional | Inflow of stock from a distribution |
| `interest` | `string \| undefined` | Optional | Inflow of cash from interest |
| `legalFee` | `string \| undefined` | Optional | Fees paid for legal charges or services |
| `longTermCapitalGain` | `string \| undefined` | Optional | Long-term capital gain received as cash |
| `managementFee` | `string \| undefined` | Optional | Fees paid for investment management of a mutual fund or other pooled investment vehicle |
| `marginExpense` | `string \| undefined` | Optional | Fees paid for maintaining margin debt |
| `nonQualifiedDividend` | `string \| undefined` | Optional | Inflow of cash from a non-qualified dividend |
| `nonResidentTax` | `string \| undefined` | Optional | Taxes paid on behalf of the investor for non-residency in investment jurisdiction |
| `pendingCredit` | `string \| undefined` | Optional | Pending inflow of cash |
| `pendingDebit` | `string \| undefined` | Optional | Pending outflow of cash |
| `qualifiedDividend` | `string \| undefined` | Optional | Inflow of cash from a qualified dividend |
| `shortTermCapitalGain` | `string \| undefined` | Optional | Short-term capital gain received as cash |
| `tax` | `string \| undefined` | Optional | Taxes paid on behalf of the investor |
| `taxWithheld` | `string \| undefined` | Optional | Taxes withheld on behalf of the customer |
| `transferFee` | `string \| undefined` | Optional | Fees incurred for transfer of a holding or account |
| `trustFee` | `string \| undefined` | Optional | Fees related to adminstration of a trust account |
| `unqualifiedGain` | `string \| undefined` | Optional | Unqualified capital gain received as cash |
| `withdrawal` | `string \| undefined` | Optional | Outflow of cash from an account |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account fee": "account fee6",
  "contribution": "contribution0",
  "deposit": "deposit6",
  "dividend": "dividend6",
  "stock distribution": "stock distribution2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

