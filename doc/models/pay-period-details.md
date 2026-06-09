
# Pay Period Details

Details about the pay period.

## Structure

`PayPeriodDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startDate` | `string \| null` | Required | The pay period start date, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format: "yyyy-mm-dd". |
| `endDate` | `string \| null` | Required | The pay period end date, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format: "yyyy-mm-dd". |
| `payDay` | `string \| null` | Required | The date on which the paystub was issued, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format ("yyyy-mm-dd"). |
| `grossEarnings` | `number \| null` | Required | Total earnings before tax. |
| `checkAmount` | `number \| null` | Required | The net amount of the paycheck. |

## Example (as JSON)

```json
{
  "start_date": "2016-03-13T12:52:32.123Z",
  "end_date": "2016-03-13T12:52:32.123Z",
  "pay_day": "2016-03-13T12:52:32.123Z",
  "gross_earnings": 169.08,
  "check_amount": 244.9
}
```

