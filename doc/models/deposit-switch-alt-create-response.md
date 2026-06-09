
# Deposit Switch Alt Create Response

DepositSwitchAltCreateResponse defines the response schema for `/deposit_switch/alt/create`

*This model accepts additional fields of type unknown.*

## Structure

`DepositSwitchAltCreateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositSwitchId` | `string` | Required | ID of the deposit switch. This ID is persisted throughout the lifetime of the deposit switch. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "deposit_switch_id": "deposit_switch_id8",
  "request_id": "request_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

