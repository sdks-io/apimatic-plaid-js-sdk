
# Earnings

An object representing both a breakdown of earnings on a paystub and the total earnings.

## Structure

`Earnings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subtotals` | [`EarningsTotal[] \| undefined`](../../doc/models/earnings-total.md) | Optional | - |
| `totals` | [`EarningsTotal[] \| undefined`](../../doc/models/earnings-total.md) | Optional | - |

## Example (as JSON)

```json
{
  "subtotals": [
    {
      "canonical_description": "OVERTIME",
      "description": "description8",
      "current_pay": {
        "amount": 45.16,
        "currency": "currency4"
      },
      "ytd_pay": {
        "amount": 28.98,
        "currency": "currency0"
      },
      "current_hours": "current_hours0"
    },
    {
      "canonical_description": "OVERTIME",
      "description": "description8",
      "current_pay": {
        "amount": 45.16,
        "currency": "currency4"
      },
      "ytd_pay": {
        "amount": 28.98,
        "currency": "currency0"
      },
      "current_hours": "current_hours0"
    },
    {
      "canonical_description": "OVERTIME",
      "description": "description8",
      "current_pay": {
        "amount": 45.16,
        "currency": "currency4"
      },
      "ytd_pay": {
        "amount": 28.98,
        "currency": "currency0"
      },
      "current_hours": "current_hours0"
    }
  ],
  "totals": [
    {
      "canonical_description": "BONUS",
      "description": "description8",
      "current_pay": {
        "amount": 45.16,
        "currency": "currency4"
      },
      "ytd_pay": {
        "amount": 28.98,
        "currency": "currency0"
      },
      "current_hours": "current_hours4"
    },
    {
      "canonical_description": "BONUS",
      "description": "description8",
      "current_pay": {
        "amount": 45.16,
        "currency": "currency4"
      },
      "ytd_pay": {
        "amount": 28.98,
        "currency": "currency0"
      },
      "current_hours": "current_hours4"
    }
  ]
}
```

