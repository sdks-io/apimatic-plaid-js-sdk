
# Income Override

Specify payroll data on the account.

## Structure

`IncomeOverride`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paystubs` | [`PaystubOverride[] \| undefined`](../../doc/models/paystub-override.md) | Optional | A list of paystubs associated with the account. |

## Example (as JSON)

```json
{
  "paystubs": [
    {
      "employer": {
        "name": "name2"
      },
      "employee": {
        "name": "name8",
        "address": {
          "city": "city6",
          "region": "region2",
          "street": "street6",
          "postal_code": "postal_code8",
          "country": "country0"
        }
      },
      "income_breakdown": [
        {
          "type": "bonus",
          "rate": 29.56,
          "hours": 6.52,
          "total": 118.76
        },
        {
          "type": "bonus",
          "rate": 29.56,
          "hours": 6.52,
          "total": 118.76
        }
      ],
      "pay_period_details": {
        "start_date": "2016-03-13T12:52:32.123Z",
        "end_date": "2016-03-13T12:52:32.123Z",
        "pay_day": "2016-03-13T12:52:32.123Z",
        "gross_earnings": 59.04,
        "check_amount": 134.86
      }
    }
  ]
}
```

