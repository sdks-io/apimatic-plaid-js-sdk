
# Transfer Authorization Decision Rationale

The rationale for Plaid's decision regarding a proposed transfer. Will be null for `approved` decisions.

## Structure

`TransferAuthorizationDecisionRationale`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | [`CodeEnum`](../../doc/models/code-enum.md) | Required | A code representing the rationale for permitting or declining the proposed transfer. Possible values are:<br><br>`NSF` – Transaction likely to result in a return due to insufficient funds.<br><br>`RISK` - Transaction is high-risk.<br><br>`MANUALLY_VERIFIED_ITEM` – Item created via same-day micro deposits, limited information available. Plaid can only offer `permitted` as a transaction decision.<br><br>`LOGIN_REQUIRED` – Unable to collect the account information required for an authorization decision due to Item staleness. Can be rectified using Link update mode.<br><br>`ERROR` – Unable to collect the account information required for an authorization decision due to an error. |
| `description` | `string` | Required | A human-readable description of the code associated with a permitted transfer or transfer decline. |

## Example (as JSON)

```json
{
  "code": "ERROR",
  "description": "description4"
}
```

