
# Income Verification Create Response

IncomeVerificationCreateResponse defines the response schema for `/income/verification/create`.

## Structure

`IncomeVerificationCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `incomeVerificationId` | `string` | Required | ID of the verification. This ID is persisted throughout the lifetime of the verification. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "income_verification_id": "income_verification_id0",
  "request_id": "request_id6"
}
```

