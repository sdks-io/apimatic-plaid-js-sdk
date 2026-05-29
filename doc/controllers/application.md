# Application

```ts
const applicationApi = new ApplicationApi(client);
```

## Class Name

`ApplicationApi`


# Application Get

Allows financial institutions to retrieve information about Plaid clients for the purpose of building control-tower experiences

```ts
async applicationGet(
  body: ApplicationGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ApplicationGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ApplicationGetRequest`](../../doc/models/application-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ApplicationGetResponse`](../../doc/models/application-get-response.md).

## Example Usage

```ts
const body: ApplicationGetRequest = {
  clientId: 'client_id8',
  secret: 'secret8',
  applicationId: 'application_id8',
};

try {
  const response = await applicationApi.applicationGet(body);

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

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response. | [`ErrorError`](../../doc/models/error-error.md) |

