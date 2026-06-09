
# Link Token Create Request Payment Initiation

Specifies options for initializing Link for use with the Payment Initiation (Europe) product. This field is required if `payment_initiation` is included in the `products` array.

## Structure

`LinkTokenCreateRequestPaymentInitiation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Required | The `payment_id` provided by the `/payment_initiation/payment/create` endpoint.<br><br>**Constraints**: *Minimum Length*: `1` |

## Example (as JSON)

```json
{
  "payment_id": "payment_id8"
}
```

