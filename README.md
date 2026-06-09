
# Getting Started with The Plaid API

## Introduction

The Plaid REST API. Please see https://plaid.com/docs/api for more details.

## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install apimatic-plaid-sdk@0.0.5
```

For additional package details, see the [Npm page for the apimatic-plaid-sdk@0.0.5 npm](https://www.npmjs.com/package/apimatic-plaid-sdk/v/0.0.5).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](doc/partial-logging-options.md) | Logging Configuration to enable logging |
| plaidClientIdCredentials | [`PlaidClientIdCredentials`](doc/auth/custom-header-signature.md) | The credential object for plaidClientId |
| plaidSecretCredentials | [`PlaidSecretCredentials`](doc/auth/custom-header-signature-1.md) | The credential object for plaidSecret |
| plaidVersionCredentials | [`PlaidVersionCredentials`](doc/auth/custom-header-signature-2.md) | The credential object for plaidVersion |

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

See the [Configuration-Based Client Initialization](doc/configuration-based-client-initialization.md) section for details.

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

See the [Environment-Based Client Initialization](doc/environment-based-client-initialization.md) section for details.

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

* [`PLAID-CLIENT-ID (Custom Header Signature)`](doc/auth/custom-header-signature.md)
* [`PLAID-SECRET (Custom Header Signature)`](doc/auth/custom-header-signature-1.md)
* [`Plaid-Version (Custom Header Signature)`](doc/auth/custom-header-signature-2.md)

## List of APIs

* [Item](doc/controllers/item.md)
* [Asset Report](doc/controllers/asset-report.md)
* [Processor](doc/controllers/processor.md)
* [Payment Initiation](doc/controllers/payment-initiation.md)
* [Sandbox](doc/controllers/sandbox.md)
* [Investments](doc/controllers/investments.md)
* [Institutions](doc/controllers/institutions.md)
* [Application](doc/controllers/application.md)
* [Accounts](doc/controllers/accounts.md)
* [Identity](doc/controllers/identity.md)
* [Liabilities](doc/controllers/liabilities.md)
* [Auth](doc/controllers/auth.md)
* [Transactions](doc/controllers/transactions.md)
* [Categories](doc/controllers/categories.md)
* [Webhook Verification Key](doc/controllers/webhook-verification-key.md)
* [Deposit Switch](doc/controllers/deposit-switch.md)
* [Link](doc/controllers/link.md)
* [Transfer](doc/controllers/transfer.md)
* [Bank Transfer](doc/controllers/bank-transfer.md)
* [Employers](doc/controllers/employers.md)
* [Income](doc/controllers/income.md)
* [Signal](doc/controllers/signal.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](doc/http-client-options.md)
* [RetryConfiguration](doc/retry-configuration.md)
* [ProxySettings](doc/proxy-settings.md)
* [Configuration-Based Client Initialization](doc/configuration-based-client-initialization.md)
* [Environment-Based Client Initialization](doc/environment-based-client-initialization.md)
* [PartialLoggingOptions](doc/partial-logging-options.md)
* [PartialRequestLoggingOptions](doc/partial-request-logging-options.md)
* [PartialResponseLoggingOptions](doc/partial-response-logging-options.md)
* [LoggerInterface](doc/logger-interface.md)

### HTTP

* [HttpRequest](doc/http-request.md)

### Utilities

* [ApiResponse](doc/api-response.md)
* [ApiError](doc/api-error.md)

