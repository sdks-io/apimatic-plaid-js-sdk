
# Item Status Transactions

Information about the last successful and failed transactions update for the Item.

## Structure

`ItemStatusTransactions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lastSuccessfulUpdate` | `string \| null \| undefined` | Optional | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) timestamp of the last successful transactions update for the Item. The status will update each time Plaid successfully connects with the institution, regardless of whether any new data is available in the update. |
| `lastFailedUpdate` | `string \| null \| undefined` | Optional | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) timestamp of the last failed transactions update for the Item. The status will update each time Plaid fails an attempt to connect with the institution, regardless of whether any new data is available in the update. |

## Example (as JSON)

```json
{
  "last_successful_update": "2016-03-13T12:52:32.123Z",
  "last_failed_update": "2016-03-13T12:52:32.123Z"
}
```

