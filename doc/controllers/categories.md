# Categories

```ts
const categoriesApi = new CategoriesApi(client);
```

## Class Name

`CategoriesApi`


# Categories Get

Send a request to the `/categories/get`  endpoint to get detailed information on categories returned by Plaid. This endpoint does not require authentication.

Find out more here: [/api/products/#categoriesget](/api/products/#categoriesget)

:information_source: **Note** This endpoint does not require authentication.

```ts
async categoriesGet(
  body: unknown,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CategoriesGetResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `unknown` | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CategoriesGetResponse`](../../doc/models/categories-get-response.md).

## Example Usage

```ts
const body = { 'key1': 'val1', 'key2': 'val2' };

try {
  const response = await categoriesApi.categoriesGet(body);

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
    if (error instanceof ErrorError) {
      console.log(error.result);
    }
  }
}
```

## Example Response *(as JSON)*

```json
{
  "categories": [
    {
      "category_id": "10000000",
      "group": "special",
      "hierarchy": [
        "Bank Fees"
      ]
    },
    {
      "category_id": "10001000",
      "group": "special",
      "hierarchy": [
        "Bank Fees",
        "Overdraft"
      ]
    },
    {
      "category_id": "12001000",
      "group": "place",
      "hierarchy": [
        "Community",
        "Animal Shelter"
      ]
    }
  ],
  "request_id": "ixTBLZGvhD4NnmB"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response. | [`ErrorError`](../../doc/models/error-error.md) |

