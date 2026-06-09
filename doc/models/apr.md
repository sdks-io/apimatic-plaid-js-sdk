
# APR

Information about the APR on the account.

## Structure

`APR`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aprPercentage` | `number` | Required | Annual Percentage Rate applied. |
| `aprType` | [`AprTypeEnum`](../../doc/models/apr-type-enum.md) | Required | The type of balance to which the APR applies. |
| `balanceSubjectToApr` | `number \| null` | Required | Amount of money that is subjected to the APR if a balance was carried beyond payment due date. How it is calculated can vary by card issuer. It is often calculated as an average daily balance. |
| `interestChargeAmount` | `number \| null` | Required | Amount of money charged due to interest from last statement. |

## Example (as JSON)

```json
{
  "apr_percentage": 181.06,
  "apr_type": "purchase_apr",
  "balance_subject_to_apr": 19.5,
  "interest_charge_amount": 108.38
}
```

