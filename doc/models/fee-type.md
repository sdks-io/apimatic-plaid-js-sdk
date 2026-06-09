
# Fee Type

Fees on the account, e.g. commission, bookkeeping, options-related.

*This model accepts additional fields of type unknown.*

## Structure

`FeeType`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountFee` | `string \| undefined` | Optional | Fees paid for account maintenance |
| `adjustment` | `string \| undefined` | Optional | Increase or decrease in quantity of item |
| `dividend` | `string \| undefined` | Optional | Inflow of cash from a dividend |
| `interest` | `string \| undefined` | Optional | Inflow of cash from interest |
| `interestReceivable` | `string \| undefined` | Optional | Inflow of cash from interest receivable |
| `longTermCapitalGain` | `string \| undefined` | Optional | Long-term capital gain received as cash |
| `legalFee` | `string \| undefined` | Optional | Fees paid for legal charges or services |
| `managementFee` | `string \| undefined` | Optional | Fees paid for investment management of a mutual fund or other pooled investment vehicle |
| `marginExpense` | `string \| undefined` | Optional | Fees paid for maintaining margin debt |
| `nonQualifiedDividend` | `string \| undefined` | Optional | Inflow of cash from a non-qualified dividend |
| `nonResidentTax` | `string \| undefined` | Optional | Taxes paid on behalf of the investor for non-residency in investment jurisdiction |
| `qualifiedDividend` | `string \| undefined` | Optional | Inflow of cash from a qualified dividend |
| `returnOfPrincipal` | `string \| undefined` | Optional | Repayment of loan principal |
| `shortTermCapitalGain` | `string \| undefined` | Optional | Short-term capital gain received as cash |
| `stockDistribution` | `string \| undefined` | Optional | Inflow of stock from a distribution |
| `tax` | `string \| undefined` | Optional | Taxes paid on behalf of the investor |
| `taxWithheld` | `string \| undefined` | Optional | Taxes withheld on behalf of the customer |
| `transferFee` | `string \| undefined` | Optional | Fees incurred for transfer of a holding or account |
| `trustFee` | `string \| undefined` | Optional | Fees related to adminstration of a trust account |
| `unqualifiedGain` | `string \| undefined` | Optional | Unqualified capital gain received as cash |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account fee": "account fee4",
  "adjustment": "adjustment4",
  "dividend": "dividend4",
  "interest": "interest0",
  "interest receivable": "interest receivable0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

