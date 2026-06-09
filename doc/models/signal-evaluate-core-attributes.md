
# Signal Evaluate Core Attributes

The core attributes object contains additional data that can be used to assess the ACH return risk, such as past ACH return events, balance/transaction history, the Item’s connection history in the Plaid network, and identity change history.

## Structure

`SignalEvaluateCoreAttributes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `unauthorizedTransactionsCount7d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to unauthorized transactions over the past 7 days from the account that will be debited. |
| `unauthorizedTransactionsCount30d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to unauthorized transactions over the past 30 days from the account that will be debited. |
| `unauthorizedTransactionsCount60d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to unauthorized transactions over the past 60 days from the account that will be debited. |
| `unauthorizedTransactionsCount90d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to unauthorized transactions over the past 90 days from the account that will be debited. |
| `nsfOverdraftTransactionsCount7d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to non-sufficient funds/overdrafts over the past 7 days from the account that will be debited. |
| `nsfOverdraftTransactionsCount30d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to non-sufficient funds/overdrafts over the past 30 days from the account that will be debited. |
| `nsfOverdraftTransactionsCount60d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to non-sufficient funds/overdrafts over the past 60 days from the account that will be debited. |
| `nsfOverdraftTransactionsCount90d` | `number \| undefined` | Optional | We parse and analyze historical transaction metadata to identify the number of possible past returns due to non-sufficient funds/overdrafts over the past 90 days from the account that will be debited. |
| `daysSinceFirstPlaidConnection` | `number \| null \| undefined` | Optional | The number of days since the first time the Item was connected to an application via Plaid |
| `plaidConnectionsCount7d` | `number \| null \| undefined` | Optional | The number of times the Item has been connected to applications via Plaid over the past 7 days |
| `plaidConnectionsCount30d` | `number \| null \| undefined` | Optional | The number of times the Item has been connected to applications via Plaid over the past 30 days |
| `totalPlaidConnectionsCount` | `number \| null \| undefined` | Optional | The total number of times the Item has been connected to applications via Plaid |
| `isSavingsOrMoneyMarketAccount` | `boolean \| undefined` | Optional | Indicates if the ACH transaction funding account is a savings/money market account |
| `totalCreditTransactionsAmount10d` | `number \| undefined` | Optional | The total credit (inflow) transaction amount over the past 10 days from the account that will be debited |
| `totalDebitTransactionsAmount10d` | `number \| undefined` | Optional | The total debit (outflow) transaction amount over the past 10 days from the account that will be debited |
| `p50CreditTransactionsAmount28d` | `number \| null \| undefined` | Optional | The 50th percentile of all credit (inflow) transaction amounts over the past 28 days from the account that will be debited |
| `p50DebitTransactionsAmount28d` | `number \| null \| undefined` | Optional | The 50th percentile of all debit (outflow) transaction amounts over the past 28 days from the account that will be debited |
| `p95CreditTransactionsAmount28d` | `number \| null \| undefined` | Optional | The 95th percentile of all credit (inflow) transaction amounts over the past 28 days from the account that will be debited |
| `p95DebitTransactionsAmount28d` | `number \| null \| undefined` | Optional | The 95th percentile of all debit (outflow) transaction amounts over the past 28 days from the account that will be debited |
| `daysWithNegativeBalanceCount90d` | `number \| null \| undefined` | Optional | The number of days within the past 90 days when the account that will be debited had a negative end-of-day available balance |
| `p90EodBalance30d` | `number \| null \| undefined` | Optional | The 90th percentile of the end-of-day available balance over the past 30 days of the account that will be debited |
| `p90EodBalance60d` | `number \| null \| undefined` | Optional | The 90th percentile of the end-of-day available balance over the past 60 days of the account that will be debited |
| `p90EodBalance90d` | `number \| null \| undefined` | Optional | The 90th percentile of the end-of-day available balance over the past 90 days of the account that will be debited |
| `p10EodBalance30d` | `number \| null \| undefined` | Optional | The 10th percentile of the end-of-day available balance over the past 30 days of the account that will be debited |
| `p10EodBalance60d` | `number \| null \| undefined` | Optional | The 10th percentile of the end-of-day available balance over the past 60 days of the account that will be debited |
| `p10EodBalance90d` | `number \| null \| undefined` | Optional | The 10th percentile of the end-of-day available balance over the past 90 days of the account that will be debited |
| `availableBalance` | `number \| null \| undefined` | Optional | Available balance, as of the `balance_last_updated` time. The available balance is the current balance less any outstanding holds or debits that have not yet posted to the account. |
| `currentBalance` | `number \| null \| undefined` | Optional | Current balance, as of the `balance_last_updated` time. The current balance is the total amount of funds in the account. |
| `balanceLastUpdated` | `string \| null \| undefined` | Optional | Timestamp in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DDTHH:mm:ssZ) indicating the last time that the balance for the given account has been updated. |
| `phoneChangeCount28d` | `number \| null \| undefined` | Optional | The number of times the account's phone numbers on file have changed over the past 28 days |
| `phoneChangeCount90d` | `number \| null \| undefined` | Optional | The number of times the account's phone numbers on file have changed over the past 90 days |
| `emailChangeCount28d` | `number \| null \| undefined` | Optional | The number of times the account's email addresses on file have changed over the past 28 days |
| `emailChangeCount90d` | `number \| null \| undefined` | Optional | The number of times the account's email addresses on file have changed over the past 90 days |
| `addressChangeCount28d` | `number \| null \| undefined` | Optional | The number of times the account's addresses on file have changed over the past 28 days |
| `addressChangeCount90d` | `number \| null \| undefined` | Optional | The number of times the account's addresses on file have changed over the past 90 days |

## Example (as JSON)

```json
{
  "unauthorized_transactions_count_7d": 214,
  "unauthorized_transactions_count_30d": 98,
  "unauthorized_transactions_count_60d": 22,
  "unauthorized_transactions_count_90d": 138,
  "nsf_overdraft_transactions_count_7d": 70
}
```

