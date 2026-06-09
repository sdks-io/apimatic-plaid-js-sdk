
# Account Identity

## Structure

`AccountIdentity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | Plaid’s unique identifier for the account. This value will not change unless Plaid can't reconcile the account with the data returned by the financial institution. This may occur, for example, when the name of the account changes. If this happens a new `account_id` will be assigned to the account.<br><br>The `account_id` can also change if the `access_token` is deleted and the same credentials that were used to generate that `access_token` are used to generate a new `access_token` on a later date. In that case, the new `account_id` will be different from the old `account_id`.<br><br>If an account with a specific `account_id` disappears instead of changing, the account is likely closed. Closed accounts are not returned by the Plaid API.<br><br>Like all Plaid identifiers, the `account_id` is case sensitive. |
| `balances` | [`AccountBalance`](../../doc/models/account-balance.md) | Required | A set of fields describing the balance for an account. Balance information may be cached unless the balance object was returned by `/accounts/balance/get`. |
| `mask` | `string \| null` | Required | The last 2-4 alphanumeric characters of an account's official account number. Note that the mask may be non-unique between an Item's accounts, and it may also not match the mask that the bank displays to the user. |
| `name` | `string` | Required | The name of the account, either assigned by the user or by the financial institution itself |
| `officialName` | `string \| null` | Required | The official name of the account as given by the financial institution |
| `type` | [`AccountTypeEnum`](../../doc/models/account-type-enum.md) | Required | `investment:` Investment account<br><br>`credit:` Credit card<br><br>`depository:` Depository account<br><br>`loan:` Loan account<br><br>`brokerage`: An investment account. Used for `/assets/` endpoints only; other endpoints use `investment`.<br><br>`other:` Non-specified account type<br><br>See the [Account type schema](https://plaid.com/docs/api/accounts#account-type-schema) for a full listing of account types and corresponding subtypes. |
| `subtype` | [`AccountSubtypeEnum`](../../doc/models/account-subtype-enum.md) | Required | See the [Account type schema](https://plaid.com/docs/api/accounts/#account-type-schema) for a full listing of account types and corresponding subtypes. |
| `verificationStatus` | [`VerificationStatus4Enum \| undefined`](../../doc/models/verification-status-4-enum.md) | Optional | The current verification status of an Auth Item initiated through Automated or Manual micro-deposits.  Returned for Auth Items only.<br><br>`pending_automatic_verification`: The Item is pending automatic verification<br><br>`pending_manual_verification`: The Item is pending manual micro-deposit verification. Items remain in this state until the user successfully verifies the two amounts.<br><br>`automatically_verified`: The Item has successfully been automatically verified<br><br>`manually_verified`: The Item has successfully been manually verified<br><br>`verification_expired`: Plaid was unable to automatically verify the deposit within 7 calendar days and will no longer attempt to validate the Item. Users may retry by submitting their information again through Link.<br><br>`verification_failed`: The Item failed manual micro-deposit verification because the user exhausted all 3 verification attempts. Users may retry by submitting their information again through Link. |
| `owners` | [`Owner[]`](../../doc/models/owner.md) | Required | Data returned by the financial institution about the account owner or owners. Only returned by Identity or Assets endpoints. Multiple owners on a single account will be represented in the same `owner` object, not in multiple owner objects within the array. |

## Example (as JSON)

```json
{
  "account_id": "account_id2",
  "balances": {
    "available": 142.32,
    "current": 79.74,
    "limit": 30.84,
    "iso_currency_code": "iso_currency_code6",
    "unofficial_currency_code": "unofficial_currency_code2",
    "last_updated_datetime": "2016-03-13T12:52:32.123Z"
  },
  "mask": "mask6",
  "name": "name0",
  "official_name": "official_name2",
  "type": "investment",
  "subtype": "mortgage",
  "owners": [
    {
      "names": [
        "names6",
        "names7"
      ],
      "phone_numbers": [
        {
          "data": "data0",
          "primary": false,
          "type": "office"
        }
      ],
      "emails": [
        {
          "data": "data6",
          "primary": false,
          "type": "other"
        }
      ],
      "addresses": [
        {
          "data": {
            "city": "city0",
            "region": "region6",
            "street": "street0",
            "postal_code": "postal_code2",
            "country": "country4"
          },
          "primary": false
        }
      ]
    }
  ],
  "verification_status": "pending_manual_verification"
}
```

