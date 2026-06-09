
# Investment Account Subtype

An investment account. Supported products for `investment` accounts are: Balance and Investments.

## Structure

`InvestmentAccountSubtype`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `m529a` | `string` | Required | Tax-advantaged college savings and prepaid tuition 529 plans (US) |
| `m401a` | `string` | Required | Employer-sponsored money-purchase 401(a) retirement plan (US) |
| `m401k` | `string` | Required | Standard 401(k) retirement account (US) |
| `m403b` | `string` | Required | 403(b) retirement savings account for non-profits and schools (US) |
| `m457b` | `string` | Required | Tax-advantaged deferred-compensation 457(b) retirement plan for governments and non-profits (US) |
| `brokerage` | `string` | Required | Standard brokerage account |
| `cashIsa` | `string` | Required | Individual Savings Account (ISA) that pays interest tax-free (UK) |
| `educationSavingsAccount` | `string` | Required | Tax-advantaged Coverdell Education Savings Account (ESA) (US) |
| `fixedAnnuity` | `string` | Required | Fixed annuity |
| `gic` | `string` | Required | Guaranteed Investment Certificate (Canada) |
| `healthReimbursementArrangement` | `string` | Required | Tax-advantaged Health Reimbursement Arrangement (HRA) benefit plan (US) |
| `hsa` | `string` | Required | Non-cash tax-advantaged medical Health Savings Account (HSA) (US) |
| `ira` | `string` | Required | Traditional Invididual Retirement Account (IRA) (US) |
| `isa` | `string` | Required | Non-cash Individual Savings Account (ISA) (UK) |
| `keogh` | `string` | Required | Keogh self-employed retirement plan (US) |
| `lif` | `string` | Required | Life Income Fund (LIF) retirement account (Canada) |
| `lifeInsurance` | `string` | Required | Life insurance account |
| `lira` | `string` | Required | Locked-in Retirement Account (LIRA) (Canada) |
| `lrif` | `string` | Required | Locked-in Retirement Income Fund (LRIF) (Canada) |
| `lrsp` | `string` | Required | Locked-in Retirement Savings Plan (Canada) |
| `mutualFund` | `string` | Required | Mutual fund account |
| `nonTaxableBrokerageAccount` | `string` | Required | A non-taxable brokerage account that is not covered by a more specific subtype |
| `other` | `string` | Required | An account whose type could not be determined |
| `otherAnnuity` | `string` | Required | An annuity account not covered by other subtypes |
| `otherInsurance` | `string` | Required | An insurance account not covered by other subtypes |
| `pension` | `string` | Required | Standard pension account |
| `prif` | `string` | Required | Prescribed Registered Retirement Income Fund (Canada) |
| `profitSharingPlan` | `string` | Required | Plan that gives employees share of company profits |
| `qshr` | `string` | Required | Qualifying share account |
| `rdsp` | `string` | Required | Registered Disability Savings Plan (RSDP) (Canada) |
| `resp` | `string` | Required | Registered Education Savings Plan (Canada) |
| `retirement` | `string` | Required | Retirement account not covered by other subtypes |
| `rlif` | `string` | Required | Restricted Life Income Fund (RLIF) (Canada) |
| `roth` | `string` | Required | Roth IRA (US) |
| `roth401k` | `string` | Required | Employer-sponsored Roth 401(k) plan (US) |
| `rrif` | `string` | Required | Registered Retirement Income Fund (RRIF) (Canada) |
| `rrsp` | `string` | Required | Registered Retirement Savings Plan (Canadian, similar to US 401(k)) |
| `sarsep` | `string` | Required | Salary Reduction Simplified Employee Pension Plan (SARSEP), discontinued retirement plan (US) |
| `sepIra` | `string` | Required | Simplified Employee Pension IRA (SEP IRA), retirement plan for small businesses and self-employed (US) |
| `simpleIra` | `string` | Required | Savings Incentive Match Plan for Employees IRA, retirement plan for small businesses (US) |
| `sipp` | `string` | Required | Self-Invested Personal Pension (SIPP) (UK) |
| `stockPlan` | `string` | Required | Standard stock plan account |
| `tfsa` | `string` | Required | Tax-Free Savings Account (TFSA), a retirement plan similar to a Roth IRA (Canada) |
| `trust` | `string` | Required | Account representing funds or assets held by a trustee for the benefit of a beneficiary. Includes both revocable and irrevocable trusts. |
| `ugma` | `string` | Required | 'Uniform Gift to Minors Act' (brokerage account for minors, US) |
| `utma` | `string` | Required | 'Uniform Transfers to Minors Act' (brokerage account for minors, US) |
| `variableAnnuity` | `string \| undefined` | Optional | Tax-deferred capital accumulation annuity contract |

## Example (as JSON)

```json
{
  "529a": "529a8",
  "401a": "401a8",
  "401k": "401k4",
  "403b": "403b6",
  "457b": "457b0",
  "brokerage": "brokerage6",
  "cash isa": "cash isa2",
  "education savings account": "education savings account6",
  "fixed annuity": "fixed annuity2",
  "gic": "gic4",
  "health reimbursement arrangement": "health reimbursement arrangement2",
  "hsa": "hsa6",
  "ira": "ira0",
  "isa": "isa8",
  "keogh": "keogh4",
  "lif": "lif4",
  "life insurance": "life insurance2",
  "lira": "lira8",
  "lrif": "lrif4",
  "lrsp": "lrsp8",
  "mutual fund": "mutual fund0",
  "non-taxable brokerage account": "non-taxable brokerage account2",
  "other": "other6",
  "other annuity": "other annuity6",
  "other insurance": "other insurance8",
  "pension": "pension8",
  "prif": "prif8",
  "profit sharing plan": "profit sharing plan8",
  "qshr": "qshr6",
  "rdsp": "rdsp0",
  "resp": "resp2",
  "retirement": "retirement0",
  "rlif": "rlif4",
  "roth": "roth8",
  "roth 401k": "roth 401k2",
  "rrif": "rrif4",
  "rrsp": "rrsp2",
  "sarsep": "sarsep0",
  "sep ira": "sep ira6",
  "simple ira": "simple ira8",
  "sipp": "sipp2",
  "stock plan": "stock plan8",
  "tfsa": "tfsa8",
  "trust": "trust8",
  "ugma": "ugma4",
  "utma": "utma2",
  "variable annuity": "variable annuity2"
}
```

