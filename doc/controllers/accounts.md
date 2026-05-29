# Accounts

```ts
const accountsApi = new AccountsApi(client);
```

## Class Name

`AccountsApi`

## Methods

* [Accounts Get](../../doc/controllers/accounts.md#accounts-get)
* [Accounts Balance Get](../../doc/controllers/accounts.md#accounts-balance-get)


# Accounts Get

The `/accounts/get`  endpoint can be used to retrieve information for any linked Item. Note that some information is nullable. Plaid will only return active bank accounts, i.e. accounts that are not closed and are capable of carrying a balance.

This endpoint retrieves cached information, rather than extracting fresh information from the institution. As a result, balances returned may not be up-to-date; for realtime balance information, use `/accounts/balance/get` instead.

Find out more here: [/api/accounts/#accountsget](/api/accounts/#accountsget)

```ts
async accountsGet(
  body: AccountsGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AccountsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`AccountsGetRequest`](../../doc/models/accounts-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AccountsGetResponse`](../../doc/models/accounts-get-response.md).

## Example Usage

```ts
const body: AccountsGetRequest = {
  accessToken: 'string',
  clientId: 'string',
  secret: 'string',
  options: {
    accountIds: [
      'string'
    ],
  },
};

try {
  const response = await accountsApi.accountsGet(body);

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


# Accounts Balance Get

The `/accounts/balance/get` endpoint returns the real-time balance for each of an Item's accounts. While other endpoints may return a balance object, only `/accounts/balance/get` forces the available and current balance fields to be refreshed rather than cached. This endpoint can be used for existing Items that were added via any of Plaid’s other products. This endpoint can be used as long as Link has been initialized with any other product, `balance` itself is not a product that can be used to initialize Link.

Find out more here: [/api/products/#accountsbalanceget](/api/products/#accountsbalanceget)

```ts
async accountsBalanceGet(
  body: AccountsBalanceGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AccountsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`AccountsBalanceGetRequest`](../../doc/models/accounts-balance-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AccountsGetResponse`](../../doc/models/accounts-get-response.md).

## Example Usage

```ts
const body: AccountsBalanceGetRequest = {
  accessToken: 'string',
  secret: 'string',
  clientId: 'string',
  options: {
    accountIds: [
      'string'
    ],
  },
};

try {
  const response = await accountsApi.accountsBalanceGet(body);

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

