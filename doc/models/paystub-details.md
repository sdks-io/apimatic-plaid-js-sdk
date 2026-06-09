
# Paystub Details

An object representing details that can be found on the paystub.

*This model accepts additional fields of type unknown.*

## Structure

`PaystubDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payPeriodStartDate` | `string \| null \| undefined` | Optional | Beginning date of the pay period on the paystub in the 'YYYY-MM-DD' format. |
| `payPeriodEndDate` | `string \| null \| undefined` | Optional | Ending date of the pay period on the paystub in the 'YYYY-MM-DD' format. |
| `payDate` | `string \| null \| undefined` | Optional | Pay date on the paystub in the 'YYYY-MM-DD' format. |
| `paystubProvider` | `string \| null \| undefined` | Optional | The name of the payroll provider that generated the paystub, e.g. ADP |
| `payFrequency` | [`PayFrequency1 \| undefined`](../../doc/models/pay-frequency-1.md) | Optional | The frequency at which the employee is paid. Possible values: `MONTHLY`, `BI-WEEKLY`, `WEEKLY`, `SEMI-MONTHLY`. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "pay_period_start_date": "2016-03-13T12:52:32.123Z",
  "pay_period_end_date": "2016-03-13T12:52:32.123Z",
  "pay_date": "2016-03-13T12:52:32.123Z",
  "paystub_provider": "paystub_provider8",
  "pay_frequency": "WEEKLY",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

