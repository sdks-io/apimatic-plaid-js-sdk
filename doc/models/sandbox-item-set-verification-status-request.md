
# Sandbox Item Set Verification Status Request

SandboxItemSetVerificationStatusRequest defines the request schema for `/sandbox/item/set_verification_status`

## Structure

`SandboxItemSetVerificationStatusRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string \| undefined` | Optional | Your Plaid API `client_id`. The `client_id` is required and may be provided either in the `PLAID-CLIENT-ID` header or as part of a request body. |
| `secret` | `string \| undefined` | Optional | Your Plaid API `secret`. The `secret` is required and may be provided either in the `PLAID-SECRET` header or as part of a request body. |
| `accessToken` | `string` | Required | The access token associated with the Item data is being requested for. |
| `accountId` | `string` | Required | The `account_id` of the account whose verification status is to be modified |
| `verificationStatus` | [`VerificationStatus1Enum`](../../doc/models/verification-status-1-enum.md) | Required | The verification status to set the account to. |

## Example (as JSON)

```json
{
  "client_id": "client_id2",
  "secret": "secret4",
  "access_token": "access_token8",
  "account_id": "account_id2",
  "verification_status": "automatically_verified"
}
```

