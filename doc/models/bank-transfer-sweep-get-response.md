
# Bank Transfer Sweep Get Response

BankTransferSweepGetResponse defines the response schema for `/bank_transfer/sweep/get`

## Structure

`BankTransferSweepGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sweep` | [`BankTransferSweep`](../../doc/models/bank-transfer-sweep.md) | Required | BankTransferSweep describes a sweep transfer. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "sweep": {
    "id": 246,
    "transfer_id": "transfer_id8",
    "created_at": "2016-03-13T12:52:32.123Z",
    "amount": "amount4",
    "iso_currency_code": "iso_currency_code4",
    "sweep_account": {
      "account_number": "account_number2",
      "routing_number": "routing_number2"
    }
  },
  "request_id": "request_id2"
}
```

