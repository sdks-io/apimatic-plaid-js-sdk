
# Custom Header Signature



Documentation for accessing and setting credentials for PLAID-SECRET.

## Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| PLAID-SECRET | `string` | - | `plaidSecret` |



**Note:** Auth credentials can be set using `plaidSecretCredentials` object in the client.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ts
import { Client } from 'apimatic-plaid-sdk';

const client = new Client({
  plaidSecretCredentials: {
    'PLAID-SECRET': 'PLAID-SECRET'
  },
});
```


