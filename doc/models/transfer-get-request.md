
# Transfer Get Request

Defines the request schema for `/transfer/get`

## Structure

`TransferGetRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `transferId` | `string` | Required | Plaid’s unique identifier for a transfer. |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "secret": "secret2",
  "transfer_id": "transfer_id2"
}
```

