
# Bank Transfer Sweep

BankTransferSweep describes a sweep transfer.

## Structure

`BankTransferSweep`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `bigint` | Required | Identifier of the sweep.<br><br>**Constraints**: `>= 0` |
| `transferId` | `string \| null` | Required | Identifier of the sweep transfer. |
| `createdAt` | `string` | Required | The datetime when the sweep occurred, in RFC 3339 format. |
| `amount` | `string` | Required | The amount of the sweep. |
| `isoCurrencyCode` | `string` | Required | The currency of the sweep, e.g. "USD". |
| `sweepAccount` | [`BankTransferSweepAccount`](../../doc/models/bank-transfer-sweep-account.md) | Required | The account where the funds are swept to. |

## Example (as JSON)

```json
{
  "id": 146,
  "transfer_id": "transfer_id4",
  "created_at": "2016-03-13T12:52:32.123Z",
  "amount": "amount0",
  "iso_currency_code": "iso_currency_code8",
  "sweep_account": {
    "account_number": "account_number2",
    "routing_number": "routing_number2"
  }
}
```

