
# Processor Apex Processor Token Create Request

ProcessorApexProcessorTokenCreateRequest defines the request schema for `/processor/apex/processor_token/create`

## Structure

`ProcessorApexProcessorTokenCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `accountId` | `string` | Required | The `account_id` value obtained from the `onSuccess` callback in Link |

## Example (as JSON)

```json
{
  "client_id": "client_id0",
  "secret": "secret6",
  "access_token": "access_token6",
  "account_id": "account_id0"
}
```

