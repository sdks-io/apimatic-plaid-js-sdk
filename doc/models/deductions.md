
# Deductions

An object with the deduction information found on a paystub.

## Structure

`Deductions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subtotals` | [`Total[] \| undefined`](../../doc/models/total.md) | Optional | - |
| `totals` | [`Total[] \| undefined`](../../doc/models/total.md) | Optional | - |

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
      }
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
      }
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
      }
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
      }
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
      }
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
      }
    }
  ]
}
```

