
# Institutions Get by Id Response

InstitutionsGetByIdResponse defines the response schema for `/institutions/get_by_id`

## Structure

`InstitutionsGetByIdResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `institution` | [`Institution`](../../doc/models/institution.md) | Required | Details relating to a specific financial institution |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "institution": {
    "institution_id": "institution_id8",
    "name": "name0",
    "products": [
      "income_verification",
      "deposit_switch",
      "standing_orders"
    ],
    "country_codes": [
      "US",
      "GB",
      "ES"
    ],
    "url": "url4",
    "primary_color": "primary_color8",
    "logo": "logo6",
    "routing_numbers": [
      "routing_numbers4",
      "routing_numbers5",
      "routing_numbers6"
    ],
    "oauth": false,
    "status": {
      "item_logins": {
        "status": "HEALTHY",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "transactions_updates": {
        "status": "DOWN",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "auth": {
        "status": "DEGRADED",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "balance": {
        "status": "DOWN",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "identity": {
        "status": "DEGRADED",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "investments_updates": {
        "status": "DEGRADED",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "liabilities_updates": {
        "status": "HEALTHY",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "liabilities": {
        "status": "DEGRADED",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "investments": {
        "status": "DOWN",
        "last_status_change": "2016-03-13T12:52:32.123Z",
        "breakdown": {
          "success": 164.84,
          "error_plaid": 201.78,
          "error_institution": 35.5,
          "refresh_interval": "NORMAL"
        }
      },
      "health_incidents": [
        {
          "start_date": "2016-03-13T12:52:32.123Z",
          "end_date": "2016-03-13T12:52:32.123Z",
          "title": "title8",
          "incident_updates": [
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            },
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            },
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            }
          ]
        },
        {
          "start_date": "2016-03-13T12:52:32.123Z",
          "end_date": "2016-03-13T12:52:32.123Z",
          "title": "title8",
          "incident_updates": [
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            },
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            },
            {
              "description": "description2",
              "status": "UNKNOWN",
              "updated_date": "2016-03-13T12:52:32.123Z"
            }
          ]
        }
      ]
    },
    "payment_initiation_metadata": {
      "supports_international_payments": false,
      "maximum_payment_amount": {
        "key0": "maximum_payment_amount9",
        "key1": "maximum_payment_amount0",
        "key2": "maximum_payment_amount1"
      },
      "supports_refund_details": false,
      "standing_order_metadata": {
        "supports_standing_order_end_date": false,
        "supports_standing_order_negative_execution_days": false,
        "valid_standing_order_intervals": [
          "WEEKLY",
          "MONTHLY"
        ]
      }
    }
  },
  "request_id": "request_id0"
}
```

