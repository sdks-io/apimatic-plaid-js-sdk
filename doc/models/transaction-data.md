
# Transaction Data

Information about the matched direct deposit transaction used to verify a user's payroll information.

## Structure

`TransactionData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string` | Required | The description of the transaction. |
| `amount` | `number` | Required | The amount of the transaction. |
| `date` | `string` | Required | The date of the transaction, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format ("yyyy-mm-dd"). |
| `accountId` | `string` | Required | A unique identifier for the end user's account. |
| `transactionId` | `string` | Required | A unique identifier for the transaction. |

## Example (as JSON)

```json
{
  "description": "description2",
  "amount": 102.84,
  "date": "2016-03-13T12:52:32.123Z",
  "account_id": "account_id4",
  "transaction_id": "transaction_id0"
}
```

