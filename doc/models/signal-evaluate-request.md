
# Signal Evaluate Request

SignalEvaluateRequest defines the request schema for `/signal/evaluate`

## Structure

`SignalEvaluateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `accountId` | `string` | Required | The `account_id` of the account whose verification status is to be modified |
| `clientTransactionId` | `string` | Required | The unique ID that you would like to use to refer to this transaction. For your convenience mapping your internal data, you could use your internal ID/identifier for this transaction. The max length for this field is 36 characters.<br><br>**Constraints**: *Maximum Length*: `36` |
| `amount` | `number` | Required | The transaction amount, in USD (e.g. `102.05`) |
| `clientUserId` | `string \| undefined` | Optional | A unique ID that identifies the end user in your system. This ID is used to correlate requests by a user with multiple Items. The max length for this field is 36 characters.<br><br>**Constraints**: *Maximum Length*: `36` |
| `user` | [`SignalUser \| undefined`](../../doc/models/signal-user.md) | Optional | Details about the end user initiating the transaction (i.e., the account holder). |
| `device` | [`SignalEvaluateDevice \| undefined`](../../doc/models/signal-evaluate-device.md) | Optional | Details about the end user's device |

## Example (as JSON)

```json
{
  "client_id": "client_id6",
  "secret": "secret0",
  "access_token": "access_token2",
  "account_id": "account_id6",
  "client_transaction_id": "client_transaction_id2",
  "amount": 215.96,
  "client_user_id": "client_user_id8",
  "user": {
    "name": {
      "prefix": "prefix8",
      "given_name": "given_name2",
      "middle_name": "middle_name0",
      "family_name": "family_name4",
      "suffix": "suffix0"
    },
    "phone_number": "phone_number2",
    "email_address": "email_address2",
    "address": {
      "city": "city6",
      "region": "region2",
      "street": "street6",
      "postal_code": "postal_code8",
      "country": "country0"
    }
  },
  "device": {
    "ip_address": "ip_address6",
    "user_agent": "user_agent8"
  }
}
```

