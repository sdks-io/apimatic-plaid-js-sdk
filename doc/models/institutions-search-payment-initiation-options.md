
# Institutions Search Payment Initiation Options

Additional options that will be used to filter institutions by various Payment Initiation configurations.

*This model accepts additional fields of type unknown.*

## Structure

`InstitutionsSearchPaymentInitiationOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string \| undefined` | Optional | A unique ID identifying the payment |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "payment_id": "payment_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

