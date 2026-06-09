
# Auth Get Numbers

An object containing identifying numbers used for making electronic transfers to and from the `accounts`. The identifying number type (ACH, EFT, IBAN, or BACS) used will depend on the country of the account. An account may have more than one number type. If a particular identifying number type is not used by any `accounts` for which data has been requested, the array for that type will be empty.

## Structure

`AuthGetNumbers`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ach` | [`NumbersACH[]`](../../doc/models/numbers-ach.md) | Required | An array of ACH numbers identifying accounts. |
| `eft` | [`NumbersEFT[]`](../../doc/models/numbers-eft.md) | Required | An array of EFT numbers identifying accounts. |
| `international` | [`NumbersInternational[]`](../../doc/models/numbers-international.md) | Required | An array of IBAN numbers identifying accounts. |
| `bacs` | [`NumbersBACS[]`](../../doc/models/numbers-bacs.md) | Required | An array of BACS numbers identifying accounts. |

## Example (as JSON)

```json
{
  "ach": [
    {
      "account_id": "account_id8",
      "account": "account6",
      "routing": "routing2",
      "wire_routing": "wire_routing4"
    }
  ],
  "eft": [
    {
      "account_id": "account_id4",
      "account": "account2",
      "institution": "institution2",
      "branch": "branch8"
    }
  ],
  "international": [
    {
      "account_id": "account_id2",
      "iban": "iban4",
      "bic": "bic2"
    }
  ],
  "bacs": [
    {
      "account_id": "account_id6",
      "account": "account4",
      "sort_code": "sort_code4"
    }
  ]
}
```

