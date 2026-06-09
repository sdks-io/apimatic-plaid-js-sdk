
# Sandbox Public Token Create Request Options Transactions

SandboxPublicTokenCreateRequestOptionsTransactions is an optional set of parameters corresponding to transactions options.

## Structure

`SandboxPublicTokenCreateRequestOptionsTransactions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startDate` | `string \| undefined` | Optional | The earliest date for which to fetch transaction history. Dates should be formatted as YYYY-MM-DD. |
| `endDate` | `string \| undefined` | Optional | The most recent date for which to fetch transaction history. Dates should be formatted as YYYY-MM-DD. |

## Example (as JSON)

```json
{
  "start_date": "2016-03-13T12:52:32.123Z",
  "end_date": "2016-03-13T12:52:32.123Z"
}
```

