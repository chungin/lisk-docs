# Lisk Elements API Client: Signatures Resource

This is a resource for interacting with the `signatures` endpoint provided by the Lisk public API. Each of the following methods can be accessed via the `signatures` property of an `APIClient` instance.

### `broadcast`

Submits a signature to sign a multisignature transaction.

#### Syntax

```js
broadcast(signatureObject)
```

#### Parameters

`signatureObject`: See details in the [Core API documentation](/lisk-core/user-guide/api/1-0/1-0.json).

#### Return value

`Promise`: Resolves to an API response object.

#### Examples

```js
client.signatures.broadcast({
    transactionId: '222675625422353767',
    publicKey: '2ca9a7143fc721fdc540fef893b27e8d648d2288efa61e56264edf01a2c23079',
    signature: '2821d93a742c4edf5fd960efad41a4def7bf0fd0f7c09869aed524f6f52bf9c97a617095e2c712bd28b4279078a29509b339ac55187854006591aa759784c205',
 })
    .then(res => {
        console.log(res.data);
    })
```
