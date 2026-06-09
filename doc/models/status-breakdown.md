
# Status Breakdown

A detailed breakdown of the institution's performance for a request type. The values for `success`, `error_plaid`, and `error_institution` sum to 1.

## Structure

`StatusBreakdown`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `number` | Required | The percentage of login attempts that are successful, expressed as a decimal. |
| `errorPlaid` | `number` | Required | The percentage of logins that are failing due to an internal Plaid issue, expressed as a decimal. |
| `errorInstitution` | `number` | Required | The percentage of logins that are failing due to an issue in the institution's system, expressed as a decimal. |
| `refreshInterval` | [`RefreshIntervalEnum \| undefined`](../../doc/models/refresh-interval-enum.md) | Optional | The `refresh_interval` may be `DELAYED` or `STOPPED` even when the success rate is high. This value is only returned for Transactions status breakdowns. |

## Example (as JSON)

```json
{
  "success": 66.52,
  "error_plaid": 103.46,
  "error_institution": 133.82,
  "refresh_interval": "STOPPED"
}
```

