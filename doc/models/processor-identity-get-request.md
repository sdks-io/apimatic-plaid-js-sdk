
# Processor Identity Get Request

ProcessorIdentityGetRequest defines the request schema for `/processor/identity/get`

*This model accepts additional fields of type unknown.*

## Structure

`ProcessorIdentityGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `processorToken` | `string` | Required | The processor token obtained from the Plaid integration partner. Processor tokens are in the format: `processor-<environment>-<identifier>` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret8",
  "processor_token": "processor_token4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

