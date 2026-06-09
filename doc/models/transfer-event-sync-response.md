
# Transfer Event Sync Response

Defines the response schema for `/transfer/event/sync`

## Structure

`TransferEventSyncResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transferEvents` | [`TransferEvent[]`](../../doc/models/transfer-event.md) | Required | - |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "transfer_events": [
    {
      "event_id": 90,
      "timestamp": "2016-03-13T12:52:32.123Z",
      "event_type": "reversed",
      "account_id": "account_id8",
      "transfer_id": "transfer_id2",
      "origination_account_id": "origination_account_id6",
      "transfer_type": "debit",
      "transfer_amount": "transfer_amount8",
      "failure_reason": {
        "ach_return_code": "ach_return_code6",
        "description": "description0"
      }
    }
  ],
  "request_id": "request_id8"
}
```

