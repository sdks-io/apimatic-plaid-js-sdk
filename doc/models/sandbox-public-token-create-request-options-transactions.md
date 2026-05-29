
# Sandbox Public Token Create Request Options Transactions

SandboxPublicTokenCreateRequestOptionsTransactions is an optional set of parameters corresponding to transactions options.

*This model accepts additional fields of type unknown.*

## Structure

`SandboxPublicTokenCreateRequestOptionsTransactions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startDate` | `string \| undefined` | Optional | The earliest date for which to fetch transaction history. Dates should be formatted as YYYY-MM-DD. |
| `endDate` | `string \| undefined` | Optional | The most recent date for which to fetch transaction history. Dates should be formatted as YYYY-MM-DD. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "start_date": "2016-03-13T12:52:32.123Z",
  "end_date": "2016-03-13T12:52:32.123Z",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

