
# Custom Header Signature



Documentation for accessing and setting credentials for Plaid-Version.

## Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| Plaid-Version | `string` | - | `plaidVersion` |



**Note:** Auth credentials can be set using `plaidVersionCredentials` object in the client.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ts
import { Client } from 'apimatic-plaid-sdk';

const client = new Client({
  plaidVersionCredentials: {
    'Plaid-Version': 'Plaid-Version'
  },
});
```


