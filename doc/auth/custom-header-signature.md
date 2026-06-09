
# Custom Header Signature



Documentation for accessing and setting credentials for PLAID-CLIENT-ID.

## Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| PLAID-CLIENT-ID | `string` | - | `plaidClientId` |



**Note:** Auth credentials can be set using `plaidClientIdCredentials` object in the client.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ts
import { Client } from 'apimatic-plaid-sdk';

const client = new Client({
  plaidClientIdCredentials: {
    'PLAID-CLIENT-ID': 'PLAID-CLIENT-ID'
  },
});
```


