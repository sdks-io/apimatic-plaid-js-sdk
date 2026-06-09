# Investments

```ts
const investmentsController = new InvestmentsController(client);
```

## Class Name

`InvestmentsController`

## Methods

* [Investments Transactions Get](../../doc/controllers/investments.md#investments-transactions-get)
* [Investments Holdings Get](../../doc/controllers/investments.md#investments-holdings-get)


# Investments Transactions Get

The `/investments/transactions/get` endpoint allows developers to retrieve user-authorized transaction data for investment accounts.

Transactions are returned in reverse-chronological order, and the sequence of transaction ordering is stable and will not shift.

Due to the potentially large number of investment transactions associated with an Item, results are paginated. Manipulate the count and offset parameters in conjunction with the `total_investment_transactions` response body field to fetch all available investment transactions.

Find out more here: [/api/products/#investmentstransactionsget](/api/products/#investmentstransactionsget)

```ts
async investmentsTransactionsGet(
  body: InvestmentsTransactionsGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InvestmentsTransactionsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`InvestmentsTransactionsGetRequest`](../../doc/models/investments-transactions-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InvestmentsTransactionsGetResponse`](../../doc/models/investments-transactions-get-response.md).

## Example Usage

```ts
const body: InvestmentsTransactionsGetRequest = {
  accessToken: 'access_token4',
  startDate: '2016-03-13T12:52:32.123Z',
  endDate: '2016-03-13T12:52:32.123Z',
};

try {
  const response = await investmentsController.investmentsTransactionsGet(body);

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


# Investments Holdings Get

The `/investments/holdings/get` endpoint allows developers to receive user-authorized stock position data for `investment`-type accounts.

Find out more here: [/api/products/#investmentsholdingsget](/api/products/#investmentsholdingsget)

```ts
async investmentsHoldingsGet(
  body: InvestmentsHoldingsGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InvestmentsHoldingsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`InvestmentsHoldingsGetRequest`](../../doc/models/investments-holdings-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InvestmentsHoldingsGetResponse`](../../doc/models/investments-holdings-get-response.md).

## Example Usage

```ts
const body: InvestmentsHoldingsGetRequest = {
  accessToken: 'access_token4',
};

try {
  const response = await investmentsController.investmentsHoldingsGet(body);

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

