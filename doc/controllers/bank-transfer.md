# Bank Transfer

```ts
const bankTransferController = new BankTransferController(client);
```

## Class Name

`BankTransferController`

## Methods

* [Bank Transfer Cancel](../../doc/controllers/bank-transfer.md#bank-transfer-cancel)
* [Bank Transfer Sweep Get](../../doc/controllers/bank-transfer.md#bank-transfer-sweep-get)
* [Bank Transfer List](../../doc/controllers/bank-transfer.md#bank-transfer-list)
* [Bank Transfer Event Sync](../../doc/controllers/bank-transfer.md#bank-transfer-event-sync)
* [Bank Transfer Migrate Account](../../doc/controllers/bank-transfer.md#bank-transfer-migrate-account)
* [Bank Transfer Create](../../doc/controllers/bank-transfer.md#bank-transfer-create)
* [Bank Transfer Sweep List](../../doc/controllers/bank-transfer.md#bank-transfer-sweep-list)
* [Bank Transfer Event List](../../doc/controllers/bank-transfer.md#bank-transfer-event-list)
* [Bank Transfer Get](../../doc/controllers/bank-transfer.md#bank-transfer-get)
* [Bank Transfer Balance Get](../../doc/controllers/bank-transfer.md#bank-transfer-balance-get)


# Bank Transfer Cancel

Use the `/bank_transfer/cancel` endpoint to cancel a bank transfer.  A transfer is eligible for cancelation if the `cancellable` property returned by `/bank_transfer/get` is `true`.

Find out more here: [/api/products#bank_transfercancel](/api/products#bank_transfercancel)

```ts
async bankTransferCancel(
  body: BankTransferCancelRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferCancelResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferCancelRequest`](../../doc/models/bank-transfer-cancel-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferCancelResponse`](../../doc/models/bank-transfer-cancel-response.md).

## Example Usage

```ts
const body: BankTransferCancelRequest = {
  bankTransferId: 'bank_transfer_id8',
};

try {
  const response = await bankTransferController.bankTransferCancel(body);

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
  "request_id": "saKrIBuEB9qJZno"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Sweep Get

The `/bank_transfer/sweep/get` endpoint fetches information about the sweep corresponding to the given `sweep_id`.

Find out more here: [/api/products#bank_transfersweepget](/api/products#bank_transfersweepget)

```ts
async bankTransferSweepGet(
  body: BankTransferSweepGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferSweepGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferSweepGetRequest`](../../doc/models/bank-transfer-sweep-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferSweepGetResponse`](../../doc/models/bank-transfer-sweep-get-response.md).

## Example Usage

```ts
const body: BankTransferSweepGetRequest = {
  sweepId: BigInt(118),
};

try {
  const response = await bankTransferController.bankTransferSweepGet(body);

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
  "sweep": {
    "id": 0,
    "transfer_id": "460cbe92-2dcc-8eae-5ad6-b37d0ec90fd9",
    "created_at": "2020-08-06T17:27:15Z",
    "amount": "12.34",
    "iso_currency_code": "USD",
    "sweep_account": {
      "account_number": "123456789",
      "routing_number": "111111111"
    }
  },
  "request_id": "saKrIBuEB9qJZno"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer List

Use the `/bank_transfer/list` endpoint to see a list of all your bank transfers and their statuses. Results are paginated; use the `count` and `offset` query parameters to retrieve the desired bank transfers.

Find out more here: [/api/products#bank_transferlist](/api/products#bank_transferlist)

```ts
async bankTransferList(
  body: BankTransferListRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferListResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferListRequest`](../../doc/models/bank-transfer-list-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferListResponse`](../../doc/models/bank-transfer-list-response.md).

## Example Usage

```ts
const body: BankTransferListRequest = {
  count: 25,
  offset: 0,
};

try {
  const response = await bankTransferController.bankTransferList(body);

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
  "bank_transfers": [
    {
      "account_id": "6qL6lWoQkAfNE3mB8Kk5tAnvpX81qefrvvl7B",
      "ach_class": "ppd",
      "amount": "12.34",
      "cancellable": true,
      "created": "2020-08-06T17:27:15Z",
      "custom_tag": "my tag",
      "description": "Testing2",
      "direction": "outbound",
      "failure_reason": {
        "ach_return_code": "R13",
        "description": "Invalid ACH routing number"
      },
      "id": "460cbe92-2dcc-8eae-5ad6-b37d0ec90fd9",
      "iso_currency_code": "USD",
      "metadata": {
        "key1": "value1",
        "key2": "value2"
      },
      "network": "ach",
      "origination_account_id": "11111111-1111-1111-1111-111111111111",
      "status": "pending",
      "type": "credit",
      "user": {
        "email_address": "plaid@plaid.com",
        "legal_name": "John Smith",
        "routing_number": "111111111"
      }
    }
  ],
  "request_id": "saKrIBuEB9qJZno"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Event Sync

`/bank_transfer/event/sync` allows you to request up to the next 25 bank transfer events that happened after a specific `event_id`. Use the `/bank_transfer/event/sync` endpoint to guarantee you have seen all bank transfer events.

Find out more here: [/api/products#bank_transfereventsync](/api/products#bank_transfereventsync)

```ts
async bankTransferEventSync(
  body: BankTransferEventSyncRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferEventSyncResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferEventSyncRequest`](../../doc/models/bank-transfer-event-sync-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferEventSyncResponse`](../../doc/models/bank-transfer-event-sync-response.md).

## Example Usage

```ts
const body: BankTransferEventSyncRequest = {
  afterId: 50,
  count: 25,
};

try {
  const response = await bankTransferController.bankTransferEventSync(body);

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
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Migrate Account

As an alternative to adding Items via Link, you can also use the `/bank_transfer/migrate_account` endpoint to migrate known account and routing numbers to Plaid Items.  Note that Items created in this way are not compatible with endpoints for other products, such as `/accounts/balance/get`, and can only be used with Bank Transfer endpoints.  If you require access to other endpoints, create the Item through Link instead.  Access to `/bank_transfer/migrate_account` is not enabled by default; to obtain access, contact your Plaid Account Manager.

Find out more here: [/api/products#bank_transfermigrate_account](/api/products#bank_transfermigrate_account)

```ts
async bankTransferMigrateAccount(
  body: BankTransferMigrateAccountRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferMigrateAccountResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferMigrateAccountRequest`](../../doc/models/bank-transfer-migrate-account-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferMigrateAccountResponse`](../../doc/models/bank-transfer-migrate-account-response.md).

## Example Usage

```ts
const body: BankTransferMigrateAccountRequest = {
  accountNumber: 'account_number4',
  routingNumber: 'routing_number0',
  accountType: 'account_type8',
};

try {
  const response = await bankTransferController.bankTransferMigrateAccount(body);

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
  "access_token": "access-sandbox-435beced-94e8-4df3-a181-1dde1cfa19f0",
  "account_id": "zvyDgbeeDluZ43AJP6m5fAxDlgoZXDuoy5gjN",
  "request_id": "mdqfuVxeoza6mhu"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Create

Use the `/bank_transfer/create` endpoint to initiate a new bank transfer.

Find out more here: [/api/products#bank_transfercreate](/api/products#bank_transfercreate)

```ts
async bankTransferCreate(
  body: BankTransferCreateRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferCreateResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferCreateRequest`](../../doc/models/bank-transfer-create-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferCreateResponse`](../../doc/models/bank-transfer-create-response.md).

## Example Usage

```ts
const body: BankTransferCreateRequest = {
  idempotencyKey: 'idempotency_key2',
  accessToken: 'access_token4',
  accountId: 'account_id8',
  type: BankTransferTypeEnum.Debit,
  network: BankTransferNetworkEnum.Samedayach,
  amount: 'amount8',
  isoCurrencyCode: 'iso_currency_code0',
  description: 'description4',
  user: {
    legalName: 'legal_name8',
  },
};

try {
  const response = await bankTransferController.bankTransferCreate(body);

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
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Sweep List

The `/bank_transfer/sweep/list` endpoint fetches information about the sweeps matching the given filters.

Find out more here: [/api/products#bank_transfersweeplist](/api/products#bank_transfersweeplist)

```ts
async bankTransferSweepList(
  body: BankTransferSweepListRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferSweepListResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferSweepListRequest`](../../doc/models/bank-transfer-sweep-list-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferSweepListResponse`](../../doc/models/bank-transfer-sweep-list-response.md).

## Example Usage

```ts
const body: BankTransferSweepListRequest = {
  count: 25,
};

try {
  const response = await bankTransferController.bankTransferSweepList(body);

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
  "sweeps": [
    {
      "id": 0,
      "transfer_id": "460cbe92-2dcc-8eae-5ad6-b37d0ec90fd9",
      "created_at": "2020-08-06T17:27:15Z",
      "amount": "12.34",
      "iso_currency_code": "USD",
      "sweep_account": {
        "account_number": "123456789",
        "routing_number": "111111111"
      }
    }
  ],
  "request_id": "saKrIBuEB9qJZno"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Event List

Use the `/bank_transfer/event/list` endpoint to get a list of bank transfer events based on specified filter criteria.

Find out more here: [/api/products#bank_transfereventlist](/api/products#bank_transfereventlist)

```ts
async bankTransferEventList(
  body: BankTransferEventListRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferEventListResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferEventListRequest`](../../doc/models/bank-transfer-event-list-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferEventListResponse`](../../doc/models/bank-transfer-event-list-response.md).

## Example Usage

```ts
const body: BankTransferEventListRequest = {
  count: 25,
  offset: 0,
};

try {
  const response = await bankTransferController.bankTransferEventList(body);

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
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Get

The `/bank_transfer/get` fetches information about the bank transfer corresponding to the given `bank_transfer_id`.

Find out more here: [/api/products#bank_transferget](/api/products#bank_transferget)

```ts
async bankTransferGet(
  body: BankTransferGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferGetRequest`](../../doc/models/bank-transfer-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferGetResponse`](../../doc/models/bank-transfer-get-response.md).

## Example Usage

```ts
const body: BankTransferGetRequest = {
  bankTransferId: 'bank_transfer_id8',
};

try {
  const response = await bankTransferController.bankTransferGet(body);

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
  "bank_transfer": {
    "account_id": "6qL6lWoQkAfNE3mB8Kk5tAnvpX81qefrvvl7B",
    "ach_class": "ppd",
    "amount": "12.34",
    "cancellable": true,
    "created": "2020-08-06T17:27:15Z",
    "custom_tag": "my tag",
    "description": "Testing2",
    "direction": "outbound",
    "failure_reason": {
      "ach_return_code": "R13",
      "description": "Invalid ACH routing number"
    },
    "id": "460cbe92-2dcc-8eae-5ad6-b37d0ec90fd9",
    "iso_currency_code": "USD",
    "metadata": {
      "key1": "value1",
      "key2": "value2"
    },
    "network": "ach",
    "origination_account_id": "11111111-1111-1111-1111-111111111111",
    "status": "pending",
    "type": "credit",
    "user": {
      "email_address": "plaid@plaid.com",
      "legal_name": "John Smith",
      "routing_number": "111111111"
    }
  },
  "request_id": "saKrIBuEB9qJZno"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |


# Bank Transfer Balance Get

Use the `/bank_transfer/balance/get` endpoint to see the available balance in your bank transfer account. Debit transfers increase this balance once their status is posted. Credit transfers decrease this balance when they are created.

The transactable balance shows the amount in your account that you are able to use for transfers, and is essentially your available balance minus your minimum balance.

Note that this endpoint can only be used with FBO accounts, when using Bank Transfers in the Full Service configuration. It cannot be used on your own account when using Bank Transfers in the BTS Platform configuration.

Find out more here: [/api/products#bank_transferbalanceget](/api/products#bank_transferbalanceget)

```ts
async bankTransferBalanceGet(
  body: BankTransferBalanceGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BankTransferBalanceGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BankTransferBalanceGetRequest`](../../doc/models/bank-transfer-balance-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BankTransferBalanceGetResponse`](../../doc/models/bank-transfer-balance-get-response.md).

## Example Usage

```ts
const body: BankTransferBalanceGetRequest = {
};

try {
  const response = await bankTransferController.bankTransferBalanceGet(body);

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
  "balance": {
    "available": "1721.70",
    "transactable": "721.70"
  },
  "origination_account_id": "11111111-1111-1111-1111-111111111111",
  "request_id": "mdqfuVxeoza6mhu"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Error response | [`ErrorError`](../../doc/models/error-error.md) |

