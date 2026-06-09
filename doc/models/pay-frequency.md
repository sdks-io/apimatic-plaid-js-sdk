
# Pay Frequency

## Structure

`PayFrequency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `value` | [`ValueEnum`](../../doc/models/value-enum.md) | Required | The frequency of the pay period. |
| `verificationStatus` | [`VerificationStatusEnum`](../../doc/models/verification-status-enum.md) | Required | The verification status. One of the following:<br><br>`"VERIFIED"`: The information was successfully verified.<br><br>`"UNVERIFIED"`: The verification has not yet been performed.<br><br>`"NEEDS_INFO"`: The verification was attempted but could not be completed due to missing information.<br><br>"`UNABLE_TO_VERIFY`": The verification was performed and the information could not be verified.<br><br>`"UNKNOWN"`: The verification status is unknown. |

## Example (as JSON)

```json
{
  "value": "weekly",
  "verification_status": "UNABLE_TO_VERIFY"
}
```

