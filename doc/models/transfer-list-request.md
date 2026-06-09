
# Transfer List Request

Defines the request schema for `/transfer/list`

## Structure

`TransferListRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `startDate` | `string \| null \| undefined` | Optional | The start datetime of transfers to list. This should be in RFC 3339 format (i.e. `2019-12-06T22:35:49Z`) |
| `endDate` | `string \| null \| undefined` | Optional | The end datetime of transfers to list. This should be in RFC 3339 format (i.e. `2019-12-06T22:35:49Z`) |
| `count` | `number \| undefined` | Optional | The maximum number of transfers to return.<br><br>**Default**: `25`<br><br>**Constraints**: `>= 1`, `<= 25` |
| `offset` | `number \| undefined` | Optional | The number of transfers to skip before returning results.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `originationAccountId` | `string \| null \| undefined` | Optional | Filter transfers to only those originated through the specified origination account. |

## Example (as JSON)

```json
{
  "count": 25,
  "offset": 0,
  "client_id": "client_id0",
  "secret": "secret4",
  "start_date": "2016-03-13T12:52:32.123Z",
  "end_date": "2016-03-13T12:52:32.123Z"
}
```

