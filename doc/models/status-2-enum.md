
# Status 2 Enum

The status of the refund.

`PROCESSING`: The refund is currently being processed. The refund will automatically exit this state when processing is complete.

`INITIATED`: The refund has been successfully initiated.

`EXECUTED`: Indicates that the refund has been successfully executed.

`FAILED`: The refund has failed to be executed. This error is retryable once the root cause is resolved.

## Enumeration

`Status2Enum`

## Fields

| Name |
|  --- |
| `PROCESSING` |
| `EXECUTED` |
| `INITIATED` |
| `FAILED` |

