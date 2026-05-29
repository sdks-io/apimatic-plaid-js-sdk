# Auth

```ts
const authApi = new AuthApi(client);
```

## Class Name

`AuthApi`


# Auth Get

The `/auth/get` endpoint returns the bank account and bank identification numbers (such as routing numbers, for US accounts) associated with an Item's checking and savings accounts, along with high-level account data and balances when available.

Note: This request may take some time to complete if `auth` was not specified as an initial product when creating the Item. This is because Plaid must communicate directly with the institution to retrieve the data.

Also note that `/auth/get` will not return data for any new accounts opened after the Item was created. To obtain data for new accounts, create a new Item.

Find out more here: [/api/products/#authget](/api/products/#authget)

```ts
async authGet(
  body: AuthGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AuthGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`AuthGetRequest`](../../doc/models/auth-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AuthGetResponse`](../../doc/models/auth-get-response.md).

## Example Usage

```ts
const body: AuthGetRequest = {
  accessToken: 'access_token4',
};

try {
  const response = await authApi.authGet(body);

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
| Default | Default error | [`ErrorError`](../../doc/models/error-error.md) |

