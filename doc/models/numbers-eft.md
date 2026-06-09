
# Numbers Eft

Identifying information for transferring money to or from a Canadian bank account via EFT.

*This model accepts additional fields of type unknown.*

## Structure

`NumbersEft`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string` | Required | The Plaid account ID associated with the account numbers |
| `account` | `string` | Required | The EFT account number for the account |
| `institution` | `string` | Required | The EFT institution number for the account |
| `branch` | `string` | Required | The EFT branch number for the account |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account_id": "account_id8",
  "account": "account6",
  "institution": "institution6",
  "branch": "branch2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

