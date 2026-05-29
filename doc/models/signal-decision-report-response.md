
# Signal Decision Report Response

SignalDecisionReportResponse defines the response schema for `/signal/decision/report`

*This model accepts additional fields of type unknown.*

## Structure

`SignalDecisionReportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

