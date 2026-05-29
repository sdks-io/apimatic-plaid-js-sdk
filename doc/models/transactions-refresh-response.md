
# Transactions Refresh Response

TransactionsRefreshResponse defines the response schema for `/transactions/refresh`

*This model accepts additional fields of type unknown.*

## Structure

`TransactionsRefreshResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "request_id": "request_id0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

