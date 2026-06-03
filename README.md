
# Getting Started with The Plaid API

## Introduction

The Plaid REST API. Please see https://plaid.com/docs/api for more details.

## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install apimatic-plaid-sdk@0.0.2
```

For additional package details, see the [Npm page for the apimatic-plaid-sdk@0.0.2 npm](https://www.npmjs.com/package/apimatic-plaid-sdk/v/0.0.2).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/partial-logging-options.md) | Logging Configuration to enable logging |
| plaidClientIdCredentials | [`PlaidClientIdCredentials`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature.md) | The credential object for plaidClientId |
| plaidSecretCredentials | [`PlaidSecretCredentials`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature-1.md) | The credential object for plaidSecret |
| plaidVersionCredentials | [`PlaidVersionCredentials`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature-2.md) | The credential object for plaidVersion |

The API client can be initialized as follows:

### Code-Based Client Initialization

```ts
import { Client, Environment, LogLevel } from 'apimatic-plaid-sdk';

const client = new Client({
  plaidClientIdCredentials: {
    'PLAID-CLIENT-ID': 'PLAID-CLIENT-ID'
  },
  plaidSecretCredentials: {
    'PLAID-SECRET': 'PLAID-SECRET'
  },
  plaidVersionCredentials: {
    'Plaid-Version': 'Plaid-Version'
  },
  timeout: 0,
  environment: Environment.Production,
  logging: {
    logLevel: LogLevel.Info,
    logRequest: {
      logBody: true
    },
    logResponse: {
      logHeaders: true
    }
  },
});
```

### Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'apimatic-plaid-sdk';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md) section for details.

### Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'apimatic-plaid-sdk';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| Production | **Default** Production |
| Environment2 | Development |
| Environment3 | Sandbox |

## Authorization

This API uses the following authentication schemes.

* [`PLAID-CLIENT-ID (Custom Header Signature)`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature.md)
* [`PLAID-SECRET (Custom Header Signature)`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature-1.md)
* [`Plaid-Version (Custom Header Signature)`](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/auth/custom-header-signature-2.md)

## List of APIs

* [Item](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/item.md)
* [Asset Report](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/asset-report.md)
* [Processor](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/processor.md)
* [Payment Initiation](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/payment-initiation.md)
* [Sandbox](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/sandbox.md)
* [Investments](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/investments.md)
* [Institutions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/institutions.md)
* [Application](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/application.md)
* [Accounts](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/accounts.md)
* [Identity](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/identity.md)
* [Liabilities](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/liabilities.md)
* [Auth](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/auth.md)
* [Transactions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/transactions.md)
* [Categories](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/categories.md)
* [Webhook Verification Key](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/webhook-verification-key.md)
* [Deposit Switch](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/deposit-switch.md)
* [Link](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/link.md)
* [Transfer](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/transfer.md)
* [Bank Transfer](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/bank-transfer.md)
* [Employers](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/employers.md)
* [Income](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/income.md)
* [Signal](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/controllers/signal.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/http-client-options.md)
* [RetryConfiguration](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/retry-configuration.md)
* [ProxySettings](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/proxy-settings.md)
* [Configuration-Based Client Initialization](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md)
* [PartialLoggingOptions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/partial-logging-options.md)
* [PartialRequestLoggingOptions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/partial-request-logging-options.md)
* [PartialResponseLoggingOptions](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/partial-response-logging-options.md)
* [LoggerInterface](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/logger-interface.md)

### HTTP

* [HttpRequest](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/api-response.md)
* [ApiError](https://www.github.com/sdks-io/apimatic-plaid-js-sdk/tree/0.0.2/doc/api-error.md)

