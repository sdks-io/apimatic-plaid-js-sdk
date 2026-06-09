
# Numbers International

Identifying information for transferring money to or from an international bank account via wire transfer.

## Structure

`NumbersInternational`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `iban` | `string` | Required | The International Bank Account Number (IBAN) for the account |
| `bic` | `string` | Required | The Bank Identifier Code (BIC) for the account |

## Example (as JSON)

```json
{
  "account_id": "account_id2",
  "iban": "iban4",
  "bic": "bic2"
}
```

