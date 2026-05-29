# Income

```ts
const incomeApi = new IncomeApi(client);
```

## Class Name

`IncomeApi`

## Methods

* [Income Verification Taxforms Get](../../doc/controllers/income.md#income-verification-taxforms-get)
* [Income Verification Paystub Get](../../doc/controllers/income.md#income-verification-paystub-get)
* [Income Verification Documents Download](../../doc/controllers/income.md#income-verification-documents-download)
* [Income Verification Refresh](../../doc/controllers/income.md#income-verification-refresh)
* [Income Verification Paystubs Get](../../doc/controllers/income.md#income-verification-paystubs-get)
* [Income Verification Precheck](../../doc/controllers/income.md#income-verification-precheck)
* [Income Verification Summary Get](../../doc/controllers/income.md#income-verification-summary-get)
* [Income Verification Create](../../doc/controllers/income.md#income-verification-create)


# Income Verification Taxforms Get

`/income/verification/taxforms/get` returns the information collected from taxforms that were used to verify an end user's. It can be called once the status of the verification has been set to `VERIFICATION_STATUS_PROCESSING_COMPLETE`, as reported by the `INCOME: verification_status` webhook. Attempting to call the endpoint before verification has been completed will result in an error.

Find out more here: [/api/products#incomeverificationtaxformsget](/api/products#incomeverificationtaxformsget)

```ts
async incomeVerificationTaxformsGet(
  body: IncomeVerificationTaxformsGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationTaxformsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationTaxformsGetRequest`](../../doc/models/income-verification-taxforms-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationTaxformsGetResponse`](../../doc/models/income-verification-taxforms-get-response.md).

## Example Usage

```ts
const body: IncomeVerificationTaxformsGetRequest = {
};

try {
  const response = await incomeApi.incomeVerificationTaxformsGet(body);

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


# Income Verification Paystub Get

(Deprecated) Retrieve information from a single paystub used for income verification

```ts
async incomeVerificationPaystubGet(
  body: IncomeVerificationPaystubGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationPaystubGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationPaystubGetRequest`](../../doc/models/income-verification-paystub-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationPaystubGetResponse`](../../doc/models/income-verification-paystub-get-response.md).

## Example Usage

```ts
const body: IncomeVerificationPaystubGetRequest = {
};

try {
  const response = await incomeApi.incomeVerificationPaystubGet(body);

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
  "request_id": "2pxQ59buGdsHRef",
  "document_metadata": {
    "name": "paystub.pdf",
    "status": "DOCUMENT_STATUS_PROCESSING_COMPLETE",
    "doc_id": "2jkflanbd"
  },
  "paystub": {
    "deductions": {
      "subtotals": [],
      "totals": []
    },
    "doc_id": "2jkflanbd",
    "earnings": {
      "subtotals": [],
      "totals": []
    },
    "employee": {
      "address": {
        "city": "SAN FRANCISCO",
        "country": "US",
        "postal_code": "94133",
        "region": "CA",
        "street": "2140 TAYLOR ST"
      },
      "name": "ANNA CHARLESTON"
    },
    "employer": {
      "name": "PLAID INC",
      "address": {
        "city": "SAN FRANCISCO",
        "country": "US",
        "postal_code": "94111",
        "region": "CA",
        "street": "1098 HARRISON ST"
      }
    },
    "employment_details": {
      "annual_salary": {
        "amount": 60000,
        "currency": "USD"
      },
      "hire_date": "2020-09-15"
    },
    "net_pay": {
      "distribution_details": [],
      "total": {
        "canonical_description": "NET PAY",
        "description": "TOTAL NET PAY",
        "ytd_pay": {
          "amount": 39456,
          "currency": "USD"
        },
        "current_pay": {
          "amount": 1490.21,
          "currency": "USD"
        }
      }
    },
    "income_breakdown": [],
    "pay_period_details": {
      "check_amount": 1490.21,
      "end_date": "2020-12-15",
      "gross_earnings": 4500,
      "pay_day": "2020-12-15",
      "start_date": "2020-12-01"
    },
    "paystub_details": {
      "pay_frequency": "BI-WEEKLY",
      "paystub_provider": "ADP",
      "pay_period_start_date": "2020-12-01",
      "pay_period_end_date": "2020-12-15",
      "pay_date": "2020-12-15"
    },
    "ytd_earnings": {
      "gross_earnings": 59375,
      "net_earnings": 39456
    }
  }
}
```


# Income Verification Documents Download

`/income/verification/documents/download` provides the ability to download the source paystub PDF that the end user uploaded via Paystub Import.

The response to `/income/verification/documents/download` is a ZIP file in binary data. The `request_id`  is returned in the `Plaid-Request-ID` header.

For Payroll Income, the most recent file available for download with the payroll provider will also be available from this endpoint.

Find out more here: [/api/products/#incomeverificationdocumentsdownload](/api/products/#incomeverificationdocumentsdownload)

```ts
async incomeVerificationDocumentsDownload(
  body: IncomeVerificationDocumentsDownloadRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<unknown>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationDocumentsDownloadRequest`](../../doc/models/income-verification-documents-download-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: A ZIP file containing the source paystub(s) used as the basis for income verification.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type `unknown`.

## Example Usage

```ts
const body: IncomeVerificationDocumentsDownloadRequest = {
};

try {
  const response = await incomeApi.incomeVerificationDocumentsDownload(body);

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


# Income Verification Refresh

`/income/verification/refresh` refreshes a given income verification.

Find out more here: [/api/products/#incomeverificationrefresh](/api/products/#incomeverificationrefresh)

```ts
async incomeVerificationRefresh(
  body: IncomeVerificationRefreshRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationRefreshResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationRefreshRequest`](../../doc/models/income-verification-refresh-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: success

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationRefreshResponse`](../../doc/models/income-verification-refresh-response.md).

## Example Usage

```ts
const body: IncomeVerificationRefreshRequest = {
};

try {
  const response = await incomeApi.incomeVerificationRefresh(body);

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


# Income Verification Paystubs Get

`/income/verification/paystubs/get` returns the information collected from the paystubs that were used to verify an end user's income. It can be called once the status of the verification has been set to `VERIFICATION_STATUS_PROCESSING_COMPLETE`, as reported by the `INCOME: verification_status` webhook. Attempting to call the endpoint before verification has been completed will result in an error.

Find out more here: [/api/products/#incomeverificationpaystubsget](/api/products/#incomeverificationpaystubsget)

```ts
async incomeVerificationPaystubsGet(
  body: IncomeVerificationPaystubsGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationPaystubsGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationPaystubsGetRequest`](../../doc/models/income-verification-paystubs-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationPaystubsGetResponse`](../../doc/models/income-verification-paystubs-get-response.md).

## Example Usage

```ts
const body: IncomeVerificationPaystubsGetRequest = {
};

try {
  const response = await incomeApi.incomeVerificationPaystubsGet(body);

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


# Income Verification Precheck

`/income/verification/precheck` returns whether a given user is supportable by the income product

```ts
async incomeVerificationPrecheck(
  body: IncomeVerificationPrecheckRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationPrecheckResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationPrecheckRequest`](../../doc/models/income-verification-precheck-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationPrecheckResponse`](../../doc/models/income-verification-precheck-response.md).

## Example Usage

```ts
const body: IncomeVerificationPrecheckRequest = {
};

try {
  const response = await incomeApi.incomeVerificationPrecheck(body);

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


# Income Verification Summary Get

`/income/verification/summary/get` returns a verification summary for the income that was verified for an end user. It can be called once the status of the verification has been set to `VERIFICATION_STATUS_PROCESSING_COMPLETE`, as reported by the `INCOME: verification_status` webhook. Attempting to call the endpoint before verification has been completed will result in an error.

Find out more here: [/api/products/#incomeverificationsummaryget](/api/products/#incomeverificationsummaryget)

```ts
async incomeVerificationSummaryGet(
  body: IncomeVerificationSummaryGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationSummaryGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationSummaryGetRequest`](../../doc/models/income-verification-summary-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationSummaryGetResponse`](../../doc/models/income-verification-summary-get-response.md).

## Example Usage

```ts
const body: IncomeVerificationSummaryGetRequest = {
};

try {
  const response = await incomeApi.incomeVerificationSummaryGet(body);

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


# Income Verification Create

`/income/verification/create` begins the income verification process by returning an `income_verification_id`. You can then provide the `income_verification_id` to `/link/token/create` under the `income_verification` parameter in order to create a Link instance that will prompt the user to go through the income verification flow. Plaid will fire an `INCOME` webhook once the user completes the Payroll Income flow, or when the uploaded documents in the Document Income flow have finished processing.

Find out more here: [/api/products/#incomeverificationcreate](/api/products/#incomeverificationcreate)

```ts
async incomeVerificationCreate(
  body: IncomeVerificationCreateRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IncomeVerificationCreateResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`IncomeVerificationCreateRequest`](../../doc/models/income-verification-create-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`IncomeVerificationCreateResponse`](../../doc/models/income-verification-create-response.md).

## Example Usage

```ts
const body: IncomeVerificationCreateRequest = {
  webhook: 'webhook4',
};

try {
  const response = await incomeApi.incomeVerificationCreate(body);

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
  "income_verification_id": "f2a826d7-25cf-483b-a124-c40beb64b732",
  "request_id": "lMjeOeu9X1VUh1F"
}
```

