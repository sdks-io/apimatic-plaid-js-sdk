
# Transactions Refresh Response

TransactionsRefreshResponse defines the response schema for `/transactions/refresh`

## Structure

`TransactionsRefreshResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "request_id": "request_id0"
}
```

