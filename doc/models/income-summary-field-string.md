
# Income Summary Field String

## Structure

`IncomeSummaryFieldString`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `value` | `string` | Required | The value of the field. |
| `verificationStatus` | [`VerificationStatusEnum`](../../doc/models/verification-status-enum.md) | Required | The verification status. One of the following:<br><br>`"VERIFIED"`: The information was successfully verified.<br><br>`"UNVERIFIED"`: The verification has not yet been performed.<br><br>`"NEEDS_INFO"`: The verification was attempted but could not be completed due to missing information.<br><br>"`UNABLE_TO_VERIFY`": The verification was performed and the information could not be verified.<br><br>`"UNKNOWN"`: The verification status is unknown. |

## Example (as JSON)

```json
{
  "value": "value6",
  "verification_status": "UNVERIFIED"
}
```

