# Webhook Verification Key

```ts
const webhookVerificationKeyApi = new WebhookVerificationKeyApi(client);
```

## Class Name

`WebhookVerificationKeyApi`


# Webhook Verification Key Get

Plaid signs all outgoing webhooks and provides JSON Web Tokens (JWTs) so that you can verify the authenticity of any incoming webhooks to your application. A message signature is included in the `Plaid-Verification` header.

The `/webhook_verification_key/get` endpoint provides a JSON Web Key (JWK) that can be used to verify a JWT.

Find out more here: [/api/webhooks/webhook-verification/#webhook_verification_keyget](/api/webhooks/webhook-verification/#webhook_verification_keyget)

```ts
async webhookVerificationKeyGet(
  body: WebhookVerificationKeyGetRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<WebhookVerificationKeyGetResponse>>
```

## Authentication

This endpoint requires [PLAID-CLIENT-ID](../../doc/auth/custom-header-signature.md) **AND** [PLAID-SECRET](../../doc/auth/custom-header-signature-1.md) **AND** [Plaid-Version](../../doc/auth/custom-header-signature-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`WebhookVerificationKeyGetRequest`](../../doc/models/webhook-verification-key-get-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`WebhookVerificationKeyGetResponse`](../../doc/models/webhook-verification-key-get-response.md).

## Example Usage

```ts
const body: WebhookVerificationKeyGetRequest = {
  keyId: 'key_id2',
};

try {
  const response = await webhookVerificationKeyApi.webhookVerificationKeyGet(body);

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
  "key": {
    "alg": "ES256",
    "created_at": 1560466150,
    "crv": "P-256",
    "expired_at": null,
    "kid": "bfbd5111-8e33-4643-8ced-b2e642a72f3c",
    "kty": "EC",
    "use": "sig",
    "x": "hKXLGIjWvCBv-cP5euCTxl8g9GLG9zHo_3pO5NN1DwQ",
    "y": "shhexqPB7YffGn6fR6h2UhTSuCtPmfzQJ6ENVIoO4Ys"
  },
  "request_id": "RZ6Omi1bzzwDaLo"
}
```

