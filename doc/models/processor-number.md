
# Processor Number

An object containing identifying numbers used for making electronic transfers to and from the `account`. The identifying number type (ACH, EFT, IBAN, or BACS) used will depend on the country of the account. An account may have more than one number type. If a particular identifying number type is not used by the `account` for which auth data has been requested, a null value will be returned.

## Structure

`ProcessorNumber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ach` | [`NumbersACHNullable \| undefined`](../../doc/models/numbers-ach-nullable.md) | Optional | - |
| `eft` | [`NumbersEFTNullable \| undefined`](../../doc/models/numbers-eft-nullable.md) | Optional | - |
| `international` | [`NumbersInternationalNullable \| undefined`](../../doc/models/numbers-international-nullable.md) | Optional | - |
| `bacs` | [`NumbersBACSNullable \| undefined`](../../doc/models/numbers-bacs-nullable.md) | Optional | - |

## Example (as JSON)

```json
{
  "ach": {
    "account_id": "account_id8",
    "account": "account6",
    "routing": "routing2",
    "wire_routing": "wire_routing4"
  },
  "eft": {
    "account_id": "account_id4",
    "account": "account2",
    "institution": "institution2",
    "branch": "branch8"
  },
  "international": {
    "account_id": "account_id2",
    "iban": "iban4",
    "bic": "bic2"
  },
  "bacs": {
    "account_id": "account_id6",
    "account": "account4",
    "sort_code": "sort_code4"
  }
}
```

