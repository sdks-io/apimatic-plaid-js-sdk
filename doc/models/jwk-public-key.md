
# JWK Public Key

A JSON Web Key (JWK) that can be used in conjunction with [JWT libraries](https://jwt.io/#libraries-io) to verify Plaid webhooks

## Structure

`JWKPublicKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alg` | `string` | Required | The alg member identifies the cryptographic algorithm family used with the key. |
| `crv` | `string` | Required | The crv member identifies the cryptographic curve used with the key. |
| `kid` | `string` | Required | The kid (Key ID) member can be used to match a specific key. This can be used, for instance, to choose among a set of keys within the JWK during key rollover. |
| `kty` | `string` | Required | The kty (key type) parameter identifies the cryptographic algorithm family used with the key, such as RSA or EC. |
| `use` | `string` | Required | The use (public key use) parameter identifies the intended use of the public key. |
| `x` | `string` | Required | The x member contains the x coordinate for the elliptic curve point. |
| `y` | `string` | Required | The y member contains the y coordinate for the elliptic curve point. |
| `createdAt` | `number` | Required | The timestamp when the key was created, in Unix time. |
| `expiredAt` | `number \| null` | Required | The timestamp when the key expired, in Unix time. |

## Example (as JSON)

```json
{
  "alg": "alg8",
  "crv": "crv0",
  "kid": "kid8",
  "kty": "kty0",
  "use": "use2",
  "x": "x8",
  "y": "y6",
  "created_at": 188,
  "expired_at": 142
}
```

