
# Recipient BACS

An object containing a BACS account number and sort code. If an IBAN is not provided or if this recipient needs to accept domestic GBP-denominated payments, BACS data is required.

## Structure

`RecipientBACS`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `string \| undefined` | Optional | The account number of the account. Maximum of 10 characters.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10` |
| `sortCode` | `string \| undefined` | Optional | The 6-character sort code of the account.<br><br>**Constraints**: *Minimum Length*: `6`, *Maximum Length*: `6` |

## Example (as JSON)

```json
{
  "account": "account6",
  "sort_code": "sort_code6"
}
```

