
# Processor Token Create Request

ProcessorTokenCreateRequest defines the request schema for `/processor/token/create`

## Structure

`ProcessorTokenCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `accountId` | `string` | Required | The `account_id` value obtained from the `onSuccess` callback in Link |
| `processor` | [`ProcessorEnum`](../../doc/models/processor-enum.md) | Required | The processor you are integrating with. |

## Example (as JSON)

```json
{
  "client_id": "client_id4",
  "secret": "secret8",
  "access_token": "access_token0",
  "account_id": "account_id4",
  "processor": "unit"
}
```

