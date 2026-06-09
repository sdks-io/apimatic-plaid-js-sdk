
# Deposit Switch Token Create Response

DepositSwitchTokenCreateResponse defines the response schema for `/deposit_switch/token/create`

*This model accepts additional fields of type unknown.*

## Structure

`DepositSwitchTokenCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositSwitchToken` | `string` | Required | Deposit switch token, used to initialize Link for the Deposit Switch product |
| `depositSwitchTokenExpirationTime` | `string` | Required | Expiration time of the token, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "deposit_switch_token": "deposit_switch_token6",
  "deposit_switch_token_expiration_time": "deposit_switch_token_expiration_time0",
  "request_id": "request_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

