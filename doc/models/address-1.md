
# Address 1

The address of the employee.

*This model accepts additional fields of type unknown.*

## Structure

`Address1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string \| undefined` | Optional | The full city name. |
| `region` | `string \| undefined` | Optional | The region or state<br>Example: `"NC"` |
| `street` | `string \| undefined` | Optional | The full street address<br>Example: `"564 Main Street, APT 15"` |
| `postalCode` | `string \| undefined` | Optional | 5 digit postal code. |
| `country` | `string \| undefined` | Optional | The country of the address. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "city": "city2",
  "region": "region8",
  "street": "street2",
  "postal_code": "postal_code4",
  "country": "country6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

