
# Numbers International

Identifying information for transferring money to or from an international bank account via wire transfer.

*This model accepts additional fields of type unknown.*

## Structure

`NumbersInternational`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `iban` | `string` | Required | The International Bank Account Number (IBAN) for the account |
| `bic` | `string` | Required | The Bank Identifier Code (BIC) for the account |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_id": "account_id2",
  "iban": "iban4",
  "bic": "bic2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

