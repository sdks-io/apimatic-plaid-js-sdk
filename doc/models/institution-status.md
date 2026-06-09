
# Institution Status

The status of an institution is determined by the health of its Item logins, Transactions updates, Investments updates, Liabilities updates, Auth requests, Balance requests, Identity requests, Investments requests, and Liabilities requests. A login attempt is conducted during the initial Item add in Link. If there is not enough traffic to accurately calculate an institution's status, Plaid will return null rather than potentially inaccurate data.

Institution status is accessible in the Dashboard and via the API using the `/institutions/get_by_id` endpoint with the `include_status` option set to true. Note that institution status is not available in the Sandbox environment.

## Structure

`InstitutionStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemLogins` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `transactionsUpdates` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `auth` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `balance` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `identity` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `investmentsUpdates` | [`ProductStatus`](../../doc/models/product-status.md) | Required | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `liabilitiesUpdates` | [`ProductStatus \| undefined`](../../doc/models/product-status.md) | Optional | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `liabilities` | [`ProductStatus \| undefined`](../../doc/models/product-status.md) | Optional | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `investments` | [`ProductStatus \| undefined`](../../doc/models/product-status.md) | Optional | A representation of the status health of a request type. Auth requests, Balance requests, Identity requests, Investments requests, Liabilities requests, Transactions updates, Investments updates, Liabilities updates, and Item logins each have their own status object. |
| `healthIncidents` | [`HealthIncident[] \| null \| undefined`](../../doc/models/health-incident.md) | Optional | Details of recent health incidents associated with the institution. |

## Example (as JSON)

```json
{
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
    }
  ]
}
```

