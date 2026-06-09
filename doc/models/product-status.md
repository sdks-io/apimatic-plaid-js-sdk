
# Product Status

A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object.

## Structure

`ProductStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`StatusEnum`](../../doc/models/status-enum.md) | Required | `HEALTHY`: the majority of requests are successful<br>`DEGRADED`: only some requests are successful<br>`DOWN`: all requests are failing |
| `lastStatusChange` | `string` | Required | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) formatted timestamp of the last status change for the institution. |
| `breakdown` | [`StatusBreakdown`](../../doc/models/status-breakdown.md) | Required | A detailed breakdown of the institution's performance for a request type. The values for `success`, `error_plaid`, and `error_institution` sum to 1. |

## Example (as JSON)

```json
{
  "status": "DEGRADED",
  "last_status_change": "2016-03-13T12:52:32.123Z",
  "breakdown": {
    "success": 164.84,
    "error_plaid": 201.78,
    "error_institution": 35.5,
    "refresh_interval": "NORMAL"
  }
}
```

