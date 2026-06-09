
# Numbers

Account and bank identifier number data used to configure the test account. All values are optional.

*This model accepts additional fields of type unknown.*

## Structure

`Numbers`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `string \| undefined` | Optional | Will be used for the account number. |
| `achRouting` | `string \| undefined` | Optional | Must be a valid ACH routing number. |
| `achWireRouting` | `string \| undefined` | Optional | Must be a valid wire transfer routing number. |
| `eftInstitution` | `string \| undefined` | Optional | EFT institution number. Must be specified alongside `eft_branch`. |
| `eftBranch` | `string \| undefined` | Optional | EFT branch number. Must be specified alongside `eft_institution`. |
| `internationalBic` | `string \| undefined` | Optional | Bank identifier code (BIC). Must be specified alongside `international_iban`. |
| `internationalIban` | `string \| undefined` | Optional | International bank account number (IBAN). If no account number is specified via `account`, will also be used as the account number by default. Must be specified alongside `international_bic`. |
| `bacsSortCode` | `string \| undefined` | Optional | BACS sort code |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "account": "account6",
  "ach_routing": "ach_routing6",
  "ach_wire_routing": "ach_wire_routing6",
  "eft_institution": "eft_institution8",
  "eft_branch": "eft_branch0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

