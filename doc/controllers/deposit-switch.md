# Deposit Switch

```ts
const depositSwitchController = new DepositSwitchController(client);
```

## Class Name

`DepositSwitchController`

## Methods

* [Deposit Switch Get](../../doc/controllers/deposit-switch.md#deposit-switch-get)
* [Deposit Switch Alt Create](../../doc/controllers/deposit-switch.md#deposit-switch-alt-create)
* [Deposit Switch Create](../../doc/controllers/deposit-switch.md#deposit-switch-create)
* [Deposit Switch Token Create](../../doc/controllers/deposit-switch.md#deposit-switch-token-create)


# Deposit Switch Get

This endpoint returns information related to how the user has configured their payroll allocation and the state of the switch. You can use this information to build logic related to the user's direct deposit allocation preferences.

Find out more here: [/api/products#deposit_switchget](/api/products#deposit_switchget)

```ts
async depositSwitchGet(
  body: DepositSwitchGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DepositSwitchGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DepositSwitchGetRequest`](../../doc/models/deposit-switch-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DepositSwitchGetResponse`](../../doc/models/deposit-switch-get-response.md).

## Example Usage

```ts
const body: DepositSwitchGetRequest = {
  depositSwitchId: 'deposit_switch_id4',
};

try {
  const response = await depositSwitchController.depositSwitchGet(body);

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
  "target_item_id": "MdRAkq1QikR3BLjDyMfMkVpqLmEm1VR7bX5hE",
  "target_account_id": "bX5hEMdRAkq1QikR3BLjDyMfMkVpqLmEm1VR7",
  "deposit_switch_id": "LjDyMfMkVpqLmEm1VR7bQikR3BX5hEMdRAkq1",
  "state": "completed",
  "switch_method": "instant",
  "date_created": "2019-11-01",
  "date_completed": "2019-11-01",
  "account_has_multiple_allocations": true,
  "is_allocated_remainder": false,
  "percent_allocated": 50,
  "amount_allocated": null,
  "employer_name": "COMPANY INC",
  "employer_id": "pqLmEm1VR7bQi11231",
  "institution_name": "Bank of America",
  "institution_id": "ins_1",
  "request_id": "lMjeOeu9X1VUh1F"
}
```


# Deposit Switch Alt Create

This endpoint provides an alternative to `/deposit_switch/create` for customers who have not yet fully integrated with Plaid Exchange. Like `/deposit_switch/create`, it creates a deposit switch entity that will be persisted throughout the lifecycle of the switch.

Find out more here: [/api/products#deposit_switchaltcreate](/api/products#deposit_switchaltcreate)

```ts
async depositSwitchAltCreate(
  body: DepositSwitchAltCreateRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DepositSwitchAltCreateResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DepositSwitchAltCreateRequest`](../../doc/models/deposit-switch-alt-create-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DepositSwitchAltCreateResponse`](../../doc/models/deposit-switch-alt-create-response.md).

## Example Usage

```ts
const body: DepositSwitchAltCreateRequest = {
  targetAccount: {
    accountNumber: 'account_number8',
    routingNumber: 'routing_number6',
    accountName: 'account_name0',
    accountSubtype: AccountSubtype1Enum.Checking,
  },
  targetUser: {
    givenName: 'given_name6',
    familyName: 'family_name8',
    phone: 'phone4',
    email: 'email2',
  },
};

try {
  const response = await depositSwitchController.depositSwitchAltCreate(body);

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
  "deposit_switch_id": "c7jMwPPManIwy9rwMewWP7lpb4pKRbtrbMomp",
  "request_id": "lMjeOeu9X1VUh1F"
}
```


# Deposit Switch Create

This endpoint creates a deposit switch entity that will be persisted throughout the lifecycle of the switch.

Find out more here: [/api/products#deposit_switchcreate](/api/products#deposit_switchcreate)

```ts
async depositSwitchCreate(
  body: DepositSwitchCreateRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DepositSwitchCreateResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DepositSwitchCreateRequest`](../../doc/models/deposit-switch-create-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DepositSwitchCreateResponse`](../../doc/models/deposit-switch-create-response.md).

## Example Usage

```ts
const body: DepositSwitchCreateRequest = {
  targetAccessToken: 'target_access_token4',
  targetAccountId: 'target_account_id2',
};

try {
  const response = await depositSwitchController.depositSwitchCreate(body);

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
  "deposit_switch_id": "c7jMwPPManIwy9rwMewWP7lpb4pKRbtrbMomp",
  "request_id": "lMjeOeu9X1VUh1F"
}
```


# Deposit Switch Token Create

In order for the end user to take action, you will need to create a public token representing the deposit switch. This token is used to initialize Link. It can be used one time and expires after 30 minutes.

Find out more here: [/deposit-switch/reference#deposit_switchtokencreate](/deposit-switch/reference#deposit_switchtokencreate)

```ts
async depositSwitchTokenCreate(
  body: DepositSwitchTokenCreateRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DepositSwitchTokenCreateResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DepositSwitchTokenCreateRequest`](../../doc/models/deposit-switch-token-create-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DepositSwitchTokenCreateResponse`](../../doc/models/deposit-switch-token-create-response.md).

## Example Usage

```ts
const body: DepositSwitchTokenCreateRequest = {
  depositSwitchId: 'deposit_switch_id4',
};

try {
  const response = await depositSwitchController.depositSwitchTokenCreate(body);

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
  "deposit_switch_token": "deposit-switch-sandbox-3e5cacca-10a6-11ea-bcdb-6003089acac0",
  "deposit_switch_token_expiration_time": "2019-12-31T12:01:37Z",
  "request_id": "68MvHx4Ub5NYoXt"
}
```

