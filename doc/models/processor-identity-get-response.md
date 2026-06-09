
# Processor Identity Get Response

ProcessorIdentityGetResponse defines the response schema for `/processor/identity/get`

## Structure

`ProcessorIdentityGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | [`AccountIdentity`](../../doc/models/account-identity.md) | Required | - |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "account": {
    "account_id": "account_id2",
    "balances": {
      "available": 142.32,
      "current": 79.74,
      "limit": 30.84,
      "iso_currency_code": "iso_currency_code6",
      "unofficial_currency_code": "unofficial_currency_code2",
      "last_updated_datetime": "2016-03-13T12:52:32.123Z"
    },
    "mask": "mask4",
    "name": "name0",
    "official_name": "official_name2",
    "type": "brokerage",
    "subtype": "tfsa",
    "owners": [
      {
        "names": [
          "names6",
          "names7"
        ],
        "phone_numbers": [
          {
            "data": "data0",
            "primary": false,
            "type": "office"
          }
        ],
        "emails": [
          {
            "data": "data6",
            "primary": false,
            "type": "other"
          }
        ],
        "addresses": [
          {
            "data": {
              "city": "city0",
              "region": "region6",
              "street": "street0",
              "postal_code": "postal_code2",
              "country": "country4"
            },
            "primary": false
          }
        ]
      }
    ],
    "verification_status": "pending_manual_verification"
  },
  "request_id": "request_id6"
}
```

