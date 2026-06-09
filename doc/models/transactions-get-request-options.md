
# Transactions Get Request Options

An optional object to be used with the request. If specified, `options` must not be `null`.

## Structure

`TransactionsGetRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountIds` | `string[] \| undefined` | Optional | A list of `account_ids` to retrieve for the Item<br><br>Note: An error will be returned if a provided `account_id` is not associated with the Item. |
| `count` | `number \| undefined` | Optional | The number of transactions to fetch.<br><br>**Default**: `100`<br><br>**Constraints**: `>= 1`, `<= 500` |
| `offset` | `number \| undefined` | Optional | The number of transactions to skip. The default value is 0.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `includeOriginalDescription` | `boolean \| null \| undefined` | Optional | Include the raw unparsed transaction description from the financial institution. This field is disabled by default. If you need this information in addition to the parsed data provided, contact your Plaid Account Manager.<br><br>**Default**: `false` |
| `includePersonalFinanceCategoryBeta` | `boolean \| undefined` | Optional | Include the `personal_finance_category` object in the response. This feature is currently in beta – to request access, contact transactions-feedback@plaid.com.<br><br>**Default**: `false` |

## Example (as JSON)

```json
{
  "count": 100,
  "offset": 0,
  "include_original_description": false,
  "include_personal_finance_category_beta": false,
  "account_ids": [
    "account_ids9"
  ]
}
```

