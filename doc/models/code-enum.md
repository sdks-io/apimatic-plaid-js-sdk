
# Code Enum

A code representing the rationale for permitting or declining the proposed transfer. Possible values are:

`NSF` – Transaction likely to result in a return due to insufficient funds.

`RISK` - Transaction is high-risk.

`MANUALLY_VERIFIED_ITEM` – Item created via same-day micro deposits, limited information available. Plaid can only offer `permitted` as a transaction decision.

`LOGIN_REQUIRED` – Unable to collect the account information required for an authorization decision due to Item staleness. Can be rectified using Link update mode.

`ERROR` – Unable to collect the account information required for an authorization decision due to an error.

## Enumeration

`CodeEnum`

## Fields

| Name |
|  --- |
| `NSF` |
| `RISK` |
| `MANUALLYVERIFIEDITEM` |
| `LOGINREQUIRED` |
| `ERROR` |

