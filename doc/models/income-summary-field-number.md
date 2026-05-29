
# Income Summary Field Number

*This model accepts additional fields of type unknown.*

## Structure

`IncomeSummaryFieldNumber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `value` | `number` | Required | The value of the field. |
| `verificationStatus` | [`VerificationStatus`](../../doc/models/verification-status.md) | Required | The verification status. One of the following:<br><br>`"VERIFIED"`: The information was successfully verified.<br><br>`"UNVERIFIED"`: The verification has not yet been performed.<br><br>`"NEEDS_INFO"`: The verification was attempted but could not be completed due to missing information.<br><br>"`UNABLE_TO_VERIFY`": The verification was performed and the information could not be verified.<br><br>`"UNKNOWN"`: The verification status is unknown. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "value": 71.84,
  "verification_status": "NEEDS_INFO",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

