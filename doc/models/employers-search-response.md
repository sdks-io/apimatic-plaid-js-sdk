
# Employers Search Response

EmployersSearchResponse defines the response schema for `/employers/search`.

## Structure

`EmployersSearchResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `employers` | [`Employer[]`](../../doc/models/employer.md) | Required | A list of employers matching the search criteria. |
| `requestId` | `string` | Required | A unique identifier for the request, which can be used for troubleshooting. This identifier, like all Plaid identifiers, is case sensitive. |

## Example (as JSON)

```json
{
  "employers": [
    {
      "employer_id": "employer_id0",
      "name": "name6",
      "address": {
        "city": "city6",
        "region": "region2",
        "street": "street6",
        "postal_code": "postal_code8",
        "country": "country0"
      },
      "confidence_score": 240.36
    }
  ],
  "request_id": "request_id2"
}
```

