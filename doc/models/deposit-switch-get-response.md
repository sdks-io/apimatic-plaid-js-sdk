
# Deposit Switch Get Response

DepositSwitchGetResponse defines the response schema for `/deposit_switch/get`

*This model accepts additional fields of type unknown.*

## Structure

`DepositSwitchGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositSwitchId` | `string` | Required | The ID of the deposit switch. |
| `targetAccountId` | `string \| null` | Required | The ID of the bank account the direct deposit was switched to. |
| `targetItemId` | `string \| null` | Required | The ID of the Item the direct deposit was switched to. |
| `state` | [`State`](../../doc/models/state.md) | Required | The state, or status, of the deposit switch.<br><br>- `initialized` – The deposit switch has been initialized with the user entering the information required to submit the deposit switch request.<br><br>- `processing` – The deposit switch request has been submitted and is being processed.<br><br>- `completed` – The user's employer has fulfilled the deposit switch request.<br><br>- `error` – There was an error processing the deposit switch request. |
| `switchMethod` | [`SwitchMethod \| undefined`](../../doc/models/switch-method.md) | Optional | The method used to make the deposit switch.<br><br>- `instant` – User instantly switched their direct deposit to a new or existing bank account by connecting their payroll or employer account.<br><br>- `mail` – User requested that Plaid contact their employer by mail to make the direct deposit switch.<br><br>- `pdf` – User generated a PDF or email to be sent to their employer with the information necessary to make the deposit switch.' |
| `accountHasMultipleAllocations` | `boolean \| null` | Required | When `true`, user’s direct deposit goes to multiple banks. When false, user’s direct deposit only goes to the target account. Always `null` if the deposit switch has not been completed. |
| `isAllocatedRemainder` | `boolean \| null` | Required | When `true`, the target account is allocated the remainder of direct deposit after all other allocations have been deducted. When `false`, user’s direct deposit is allocated as a percent or amount. Always `null` if the deposit switch has not been completed. |
| `percentAllocated` | `number \| null` | Required | The percentage of direct deposit allocated to the target account. Always `null` if the target account is not allocated a percentage or if the deposit switch has not been completed or if `is_allocated_remainder` is true. |
| `amountAllocated` | `number \| null` | Required | The dollar amount of direct deposit allocated to the target account. Always `null` if the target account is not allocated an amount or if the deposit switch has not been completed. |
| `employerName` | `string \| null \| undefined` | Optional | The name of the employer selected by the user. If the user did not select an employer, the value returned is `null`. |
| `employerId` | `string \| null \| undefined` | Optional | The ID of the employer selected by the user. If the user did not select an employer, the value returned is `null`. |
| `institutionName` | `string \| null \| undefined` | Optional | The name of the institution selected by the user. If the user did not select an institution, the value returned is `null`. |
| `institutionId` | `string \| null \| undefined` | Optional | The ID of the institution selected by the user. If the user did not select an institution, the value returned is `null`. |
| `dateCreated` | `string` | Required | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) date the deposit switch was created. |
| `dateCompleted` | `string \| null` | Required | [ISO 8601](https://wikipedia.org/wiki/ISO_8601) date the deposit switch was completed. Always `null` if the deposit switch has not been completed. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "deposit_switch_id": "deposit_switch_id8",
  "target_account_id": "target_account_id8",
  "target_item_id": "target_item_id4",
  "state": "initialized",
  "switch_method": "instant",
  "account_has_multiple_allocations": false,
  "is_allocated_remainder": false,
  "percent_allocated": 158.22,
  "amount_allocated": 250.66,
  "employer_name": "employer_name4",
  "employer_id": "employer_id4",
  "institution_name": "institution_name6",
  "institution_id": "institution_id8",
  "date_created": "2016-03-13T12:52:32.123Z",
  "date_completed": "2016-03-13T12:52:32.123Z",
  "request_id": "request_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

