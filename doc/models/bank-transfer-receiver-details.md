
# Bank Transfer Receiver Details

The receiver details if the type of this event is `reciever_pending` or `reciever_posted`. Null value otherwise.

## Structure

`BankTransferReceiverDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `availableBalance` | [`AvailableBalanceEnum`](../../doc/models/available-balance-enum.md) | Required | The sign of the available balance for the receiver bank account associated with the receiver event at the time the matching transaction was found. Can be `positive`, `negative`, or null if the balance was not available at the time. |

## Example (as JSON)

```json
{
  "available_balance": "positive"
}
```

