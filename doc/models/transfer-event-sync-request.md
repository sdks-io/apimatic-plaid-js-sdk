
# Transfer Event Sync Request

Defines the request schema for `/transfer/event/sync`

## Structure

`TransferEventSyncRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `afterId` | `number` | Required | The latest (largest) `event_id` fetched via the sync endpoint, or 0 initially.<br><br>**Constraints**: `>= 0` |
| `count` | `number \| null \| undefined` | Optional | The maximum number of transfer events to return.<br><br>**Default**: `25`<br><br>**Constraints**: `>= 1`, `<= 25` |

## Example (as JSON)

```json
{
  "after_id": 132,
  "count": 25,
  "client_id": "client_id6",
  "secret": "secret0"
}
```

