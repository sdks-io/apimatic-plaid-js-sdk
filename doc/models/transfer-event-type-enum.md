
# Transfer Event Type Enum

The type of event that this transfer represents.

`pending`: A new transfer was created; it is in the pending state.

`cancelled`: The transfer was cancelled by the client.

`failed`: The transfer failed, no funds were moved.

`posted`: The transfer has been successfully submitted to the payment network.

`reversed`: A posted transfer was reversed.

## Enumeration

`TransferEventTypeEnum`

## Fields

| Name |
|  --- |
| `Pending` |
| `Cancelled` |
| `Failed` |
| `Posted` |
| `Reversed` |

