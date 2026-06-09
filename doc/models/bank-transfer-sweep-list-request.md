
# Bank Transfer Sweep List Request

BankTransferSweepListRequest defines the request schema for `/bank_transfer/sweep/list`

*This model accepts additional fields of type unknown.*

## Structure

`BankTransferSweepListRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `originationAccountId` | `string \| null \| undefined` | Optional | If multiple origination accounts are available, `origination_account_id` must be used to specify the account that the sweeps belong to. |
| `startId` | `number \| null \| undefined` | Optional | Starting ID of sweeps to return.<br><br>**Constraints**: `>= 0` |
| `startTime` | `string \| null \| undefined` | Optional | The start datetime of sweeps to return (RFC 3339 format). |
| `endTime` | `string \| null \| undefined` | Optional | The end datetime of sweeps to return (RFC 3339 format). |
| `count` | `number \| null \| undefined` | Optional | The maximum number of sweeps to return.<br><br>**Default**: `25`<br><br>**Constraints**: `>= 1`, `<= 25` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "count": 25,
  "client_id": "client_id4",
  "secret": "secret8",
  "origination_account_id": "origination_account_id2",
  "start_id": 4,
  "start_time": "2016-03-13T12:52:32.123Z",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

