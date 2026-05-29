
# Processor Token Create Response

ProcessorTokenCreateResponse defines the response schema for `/processor/token/create` and `/processor/apex/processor_token/create`

*This model accepts additional fields of type unknown.*

## Structure

`ProcessorTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `processorToken` | `string` | Required | The `processor_token` that can then be used by the Plaid partner to make API requests |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "processor_token": "processor_token8",
  "request_id": "request_id6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

