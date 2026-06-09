
# Student Loan Status

An object representing the status of the student loan

## Structure

`StudentLoanStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endDate` | `string \| null` | Required | The date until which the loan will be in its current status. Dates are returned in an [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `type` | [`Type2Enum`](../../doc/models/type-2-enum.md) | Required | The status type of the student loan |

## Example (as JSON)

```json
{
  "end_date": "2016-03-13T12:52:32.123Z",
  "type": "paid in full"
}
```

