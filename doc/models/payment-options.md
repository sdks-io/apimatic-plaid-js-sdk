
# Payment Options

Additional payment options

## Structure

`PaymentOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestRefundDetails` | `boolean \| null \| undefined` | Optional | When `true`, Plaid will attempt to request refund details from the payee's financial institution.  Support varies between financial institutions and will not always be available.  If refund details could be retrieved, they will be available in the `/payment_initiation/payment/get` response. |
| `iban` | `string \| null \| undefined` | Optional | The International Bank Account Number (IBAN) for the payer's account. If provided, the end user will be able to send payments only from the specified bank account.<br><br>**Constraints**: *Minimum Length*: `15`, *Maximum Length*: `34` |
| `bacs` | [`PaymentInitiationOptionalRestrictionBacs \| undefined`](../../doc/models/payment-initiation-optional-restriction-bacs.md) | Optional | - |
| `emiAccountId` | `string \| null \| undefined` | Optional | The EMI (E-Money Institution) account that this payment is associated with, if any. This EMI account is used as an intermediary account to enable Plaid to reconcile the settlement of funds for Payment Initiation requests.<br><br>**Constraints**: *Minimum Length*: `1` |

## Example (as JSON)

```json
{
  "request_refund_details": false,
  "iban": "iban8",
  "bacs": {
    "account": "account4",
    "sort_code": "sort_code4"
  },
  "emi_account_id": "emi_account_id2"
}
```

