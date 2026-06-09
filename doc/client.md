
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](../doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| pLAIDCLIENTIDCredentials | [`PLAIDCLIENTIDCredentials`](auth/custom-header-signature.md) | The credential object for pLAIDCLIENTID |
| pLAIDSECRETCredentials | [`PLAIDSECRETCredentials`](auth/custom-header-signature-1.md) | The credential object for pLAIDSECRET |
| plaidVersionCredentials | [`PlaidVersionCredentials`](auth/custom-header-signature-2.md) | The credential object for plaidVersion |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ts
import { Client, Environment } from 'apimatic-plaid-sdk';

const client = new Client({
  pLAIDCLIENTIDCredentials: {
    'PLAID-CLIENT-ID': 'PLAID-CLIENT-ID'
  },
  pLAIDSECRETCredentials: {
    'PLAID-SECRET': 'PLAID-SECRET'
  },
  plaidVersionCredentials: {
    'Plaid-Version': 'Plaid-Version'
  },
  timeout: 0,
  environment: Environment.Production,
});
```

## Configuration-Based Client Initialization

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

See the [Configuration-Based Client Initialization](../doc/configuration-based-client-initialization.md) section for details.

## Environment-Based Client Initialization

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

See the [Environment-Based Client Initialization](../doc/environment-based-client-initialization.md) section for details.

