
# Signal Evaluate Device

Details about the end user's device

*This model accepts additional fields of type unknown.*

## Structure

`SignalEvaluateDevice`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipAddress` | `string \| null \| undefined` | Optional | The IP address of the device that initiated the transaction |
| `userAgent` | `string \| null \| undefined` | Optional | The user agent of the device that initiated the transaction (e.g. "Mozilla/5.0") |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "ip_address": "ip_address8",
  "user_agent": "user_agent0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

