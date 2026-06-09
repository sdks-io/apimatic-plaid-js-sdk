
# Transfer Failure

The failure reason if the type of this transfer is `"failed"` or `"reversed"`. Null value otherwise.

## Structure

`TransferFailure`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `achReturnCode` | `string \| null \| undefined` | Optional | The ACH return code, e.g. `R01`.  A return code will be provided if and only if the transfer status is `reversed`. For a full listing of ACH return codes, see [Bank Transfers errors](https://plaid.com/docs/errors/bank-transfers/#ach-return-codes). |
| `description` | `string \| undefined` | Optional | A human-readable description of the reason for the failure or reversal. |

## Example (as JSON)

```json
{
  "ach_return_code": "ach_return_code4",
  "description": "description8"
}
```

