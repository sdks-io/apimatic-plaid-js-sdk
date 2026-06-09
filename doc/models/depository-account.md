
# Depository Account

An account type holding cash, in which funds are deposited. Supported products for `depository` accounts are: Auth, Balance, Transactions, Identity, Payment Initiation, and Assets.

## Structure

`DepositoryAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checking` | `string` | Required | Checking account |
| `savings` | `string` | Required | Savings account |
| `hsa` | `string` | Required | Health Savings Account (US only) that can only hold cash |
| `cd` | `string` | Required | Certificate of deposit account |
| `moneyMarket` | `string` | Required | Money market account |
| `paypal` | `string` | Required | PayPal depository account |
| `prepaid` | `string` | Required | Prepaid debit card |
| `cashManagement` | `string` | Required | A cash management account, typically a cash account at a brokerage |
| `ebt` | `string` | Required | An Electronic Benefit Transfer (EBT) account, used by certain public assistance programs to distribute funds (US only) |

## Example (as JSON)

```json
{
  "checking": "checking2",
  "savings": "savings4",
  "hsa": "hsa2",
  "cd": "cd0",
  "money market": "money market8",
  "paypal": "paypal2",
  "prepaid": "prepaid8",
  "cash management": "cash management8",
  "ebt": "ebt0"
}
```

