
# Processor Balance Get Request

ProcessorBalanceGetRequest defines the request schema for `/processor/balance/get`

## Structure

`ProcessorBalanceGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `processorToken` | `string` | Required | The processor token obtained from the Plaid integration partner. Processor tokens are in the format: `processor-<environment>-<identifier>` |
| `options` | [`ProcessorBalanceGetRequestOptions \| undefined`](../../doc/models/processor-balance-get-request-options.md) | Optional | An optional object to filter `/processor/balance/get` results. |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "processor_token": "processor_token6",
  "options": {
    "min_last_updated_datetime": "2016-03-13T12:52:32.123Z"
  }
}
```

