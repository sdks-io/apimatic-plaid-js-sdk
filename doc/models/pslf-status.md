
# Pslf Status

Information about the student's eligibility in the Public Service Loan Forgiveness program. This is only returned if the institution is Fedloan (`ins_116527`).

*This model accepts additional fields of type unknown.*

## Structure

`PslfStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `estimatedEligibilityDate` | `string \| null` | Required | The estimated date borrower will have completed 120 qualifying monthly payments. Returned in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format (YYYY-MM-DD). |
| `paymentsMade` | `number \| null` | Required | The number of qualifying payments that have been made. |
| `paymentsRemaining` | `number \| null` | Required | The number of qualifying payments remaining. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "estimated_eligibility_date": "2016-03-13T12:52:32.123Z",
  "payments_made": 18.4,
  "payments_remaining": 64.38,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

