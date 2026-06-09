
# Bank Transfer

Represents a bank transfer within the Bank Transfers API.

## Structure

`BankTransfer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Plaid’s unique identifier for a bank transfer. |
| `achClass` | [`ACHClassEnum`](../../doc/models/ach-class-enum.md) | Required | Specifies the use case of the transfer.  Required for transfers on an ACH network.<br><br>`"arc"` - Accounts Receivable Entry<br><br>`"cbr`" - Cross Border Entry<br><br>`"ccd"` - Corporate Credit or Debit - fund transfer between two corporate bank accounts<br><br>`"cie"` - Customer Initiated Entry<br><br>`"cor"` - Automated Notification of Change<br><br>`"ctx"` - Corporate Trade Exchange<br><br>`"iat"` - International<br><br>`"mte"` - Machine Transfer Entry<br><br>`"pbr"` - Cross Border Entry<br><br>`"pop"` - Point-of-Purchase Entry<br><br>`"pos"` - Point-of-Sale Entry<br><br>`"ppd"` - Prearranged Payment or Deposit - the transfer is part of a pre-existing relationship with a consumer, eg. bill payment<br><br>`"rck"` - Re-presented Check Entry<br><br>`"tel"` - Telephone-Initiated Entry<br><br>`"web"` - Internet-Initiated Entry - debits from a consumer’s account where their authorization is obtained over the Internet |
| `accountId` | `string` | Required | The account ID that should be credited/debited for this bank transfer. |
| `type` | [`BankTransferTypeEnum`](../../doc/models/bank-transfer-type-enum.md) | Required | The type of bank transfer. This will be either `debit` or `credit`.  A `debit` indicates a transfer of money into the origination account; a `credit` indicates a transfer of money out of the origination account. |
| `user` | [`BankTransferUser`](../../doc/models/bank-transfer-user.md) | Required | The legal name and other information for the account holder. |
| `amount` | `string` | Required | The amount of the bank transfer (decimal string with two digits of precision e.g. “10.00”). |
| `isoCurrencyCode` | `string` | Required | The currency of the transfer amount, e.g. "USD" |
| `description` | `string` | Required | The description of the transfer. |
| `created` | `string` | Required | The datetime when this bank transfer was created. This will be of the form `2006-01-02T15:04:05Z` |
| `status` | [`BankTransferStatusEnum`](../../doc/models/bank-transfer-status-enum.md) | Required | The status of the transfer. |
| `network` | [`BankTransferNetworkEnum`](../../doc/models/bank-transfer-network-enum.md) | Required | The network or rails used for the transfer. Valid options are `ach`, `same-day-ach`, or `wire`. |
| `cancellable` | `boolean` | Required | When `true`, you can still cancel this bank transfer. |
| `failureReason` | [`BankTransferFailure`](../../doc/models/bank-transfer-failure.md) | Required | The failure reason if the type of this transfer is `"failed"` or `"reversed"`. Null value otherwise. |
| `customTag` | `string \| null` | Required | A string containing the custom tag provided by the client in the create request. Will be null if not provided. |
| `metadata` | `Record<string, string>` | Required | The Metadata object is a mapping of client-provided string fields to any string value. The following limitations apply:<br><br>- The JSON values must be Strings (no nested JSON objects allowed)<br>- Only ASCII characters may be used<br>- Maximum of 50 key/value pairs<br>- Maximum key length of 40 characters<br>- Maximum value length of 500 characters |
| `originationAccountId` | `string` | Required | Plaid’s unique identifier for the origination account that was used for this transfer. |
| `direction` | [`BankTransferDirectionEnum`](../../doc/models/bank-transfer-direction-enum.md) | Required | Indicates the direction of the transfer: `outbound` for API-initiated transfers, or `inbound` for payments received by the FBO account. |

## Example (as JSON)

```json
{
  "id": "id0",
  "ach_class": "cbr",
  "account_id": "account_id2",
  "type": "debit",
  "user": {
    "legal_name": "legal_name8",
    "email_address": "email_address2",
    "routing_number": "routing_number4"
  },
  "amount": "amount2",
  "iso_currency_code": "iso_currency_code6",
  "description": "description0",
  "created": "2016-03-13T12:52:32.123Z",
  "status": "cancelled",
  "network": "same-day-ach",
  "cancellable": false,
  "failure_reason": {
    "ach_return_code": "ach_return_code6",
    "description": "description0"
  },
  "custom_tag": "custom_tag2",
  "metadata": {
    "key0": "metadata7",
    "key1": "metadata6",
    "key2": "metadata5"
  },
  "origination_account_id": "origination_account_id0",
  "direction": "outbound"
}
```

