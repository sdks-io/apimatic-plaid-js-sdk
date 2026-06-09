
# Bank Transfer Balance

## Structure

`BankTransferBalance`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `string` | Required | The total available balance - the sum of all successful debit transfer amounts minus all credit transfer amounts. |
| `transactable` | `string` | Required | The transactable balance shows the amount in your account that you are able to use for transfers, and is essentially your available balance minus your minimum balance. |

## Example (as JSON)

```json
{
  "available": "available2",
  "transactable": "transactable2"
}
```

