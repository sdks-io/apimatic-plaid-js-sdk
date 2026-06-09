
# Employer

Data about the employer.

## Structure

`Employer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `employerId` | `string` | Required | Plaid's unique identifier for the employer. |
| `name` | `string` | Required | The name of the employer |
| `address` | [`AddressDataNullable`](../../doc/models/address-data-nullable.md) | Required | - |
| `confidenceScore` | `number` | Required | A number from 0 to 1 indicating Plaid's level of confidence in the pairing between the employer and the institution (not yet implemented). |

## Example (as JSON)

```json
{
  "employer_id": "employer_id0",
  "name": "name6",
  "address": {
    "city": "city6",
    "region": "region2",
    "street": "street6",
    "postal_code": "postal_code8",
    "country": "country0"
  },
  "confidence_score": 116.56
}
```

