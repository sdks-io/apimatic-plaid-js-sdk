
# Numbers Eft Nullable

*This model accepts additional fields of type unknown.*

## Structure

`NumbersEftNullable`

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
  "account_id": "account_id0",
  "account": "account8",
  "institution": "institution8",
  "branch": "branch4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

