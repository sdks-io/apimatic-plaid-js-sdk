# Employers

```ts
const employersController = new EmployersController(client);
```

## Class Name

`EmployersController`


# Employers Search

`/employers/search` allows you the ability to search Plaid’s database of known employers, for use with Deposit Switch. You can use this endpoint to look up a user's employer in order to confirm that they are supported. Users with non-supported employers can then be routed out of the Deposit Switch flow.

The data in the employer database is currently limited. As the Deposit Switch and Income products progress through their respective beta periods, more employers are being regularly added. Because the employer database is frequently updated, we recommend that you do not cache or store data from this endpoint for more than a day.

Find out more here: [/api/employers/#employerssearch](/api/employers/#employerssearch)

```ts
async employersSearch(
  body: EmployersSearchRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<EmployersSearchResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`EmployersSearchRequest`](../../doc/models/employers-search-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`EmployersSearchResponse`](../../doc/models/employers-search-response.md).

## Example Usage

```ts
const body: EmployersSearchRequest = {
  query: 'query6',
  products: [
    'products4'
  ],
};

try {
  const response = await employersController.employersSearch(body);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Example Response *(as JSON)*

```json
{
  "employers": [
    {
      "name": "Plaid Inc.",
      "address": {
        "city": "San Francisco",
        "country": "US",
        "postal_code": "94103",
        "region": "CA",
        "street": "1098 Harrison St"
      },
      "confidence_score": 1,
      "employer_id": "emp_1"
    }
  ],
  "request_id": "ixTBLZGvhD4NnmB"
}
```

