
# Taxpayer ID

## Structure

`TaxpayerID`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idType` | `string \| null \| undefined` | Optional | Type of ID, e.g. 'SSN' |
| `last4Digits` | `string \| null \| undefined` | Optional | Last 4 digits of unique number of ID.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `4` |

## Example (as JSON)

```json
{
  "id_type": "id_type4",
  "last_4_digits": "last_4_digits0"
}
```

