# JSON Web Tokens (JWT)

JWT - compact, digitally signed, self-contained way of transmitting info between parties (can be encrypted).
- Header - carries token type(JWT in this case) and algorithm used for signature
```
{
    "alg": "HS256",
    "typ": "JWT"
}
```

- Payload - contains claims about the entity
  - registered claim - optional set of predefined claims about issuer, expiration time, subject, audience, etc.
  - public claim - can be defined by the coder using the JWT, but should be publicly defined in IANA JSON Token Registry, or as a URI that gets the JWT past the collision of mismatched claims.
  - private claim - claims created by and between 2 agreeing parties.
```
<!-- this example of a payload would then be Base64Url encoded to form signature -->
{
    "sub": "1234567890",
    "name": "John Doe",
    "admin": true
}
```

- Signature - is a signed document containing the encoded header, encoded payload, a secret, and the algorithm in the header. Because it contains the encoded body of the message the signature also works to confirm that the message has arrived unchanged.
```
<!-- To create signature -->
HMACSHA256(
    base64urlEncode(header) + "." + base64UrlEncode(payload),
    secret)
```

HMAC - one algorithm used to encode/decode the digital signature.

Authorization - Tokens are used for authorization for users as well. The token is sent when they log in (typically in the Authorization header as shown below) and should be deleted as soon as reasonably possible to avoid security breaches.
```
Authorization: Bearer <token>

CORS exists in python (makes sense)

websites log you out after a while because the token expired. refreshing with a reset token can get you in again.