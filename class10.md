## User Modeling
* Web developers have a duty to safely handle information
* Cryptography is the science of encoding messages
* A Cryptographic Hash Algorithm takes a piece of data and produces a hash that is deliberately difficult to reverse, if identical data is passed to it the same hash will always be returned
* It takes a piece of data and a key to produce encrypted data Later the data can be reversed into the original data by decrypting it using the same key
* User tokens can be created by associating a random unique string (tokenSeed) with a user account and encrypting the tokenSeed with a secret key that only the server knows, then the encrypted token gets sent to a client application. The app then uses the token to make requests
* Basic authorization is a common method used to send passwords and usernames on HTTP requests
* The username and password is joined and then base64 encoded using atob and btoa
* let encoded = window.btoa('someusername:P@55w0rD!')
* let decoded = window.atob('c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==');

## Basic Access Authentication
* Basic Authentication doesn't provide any confidentiality protection, they are only encoded in base64 in transit. It must be used with HTTPS to provide confidentiality

## Intro to JWT (JSON Web Token)
* JWT is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. It can be verified and trusted because it is digitally signed using a secret (HMAC algorithm) or public/private key pair using RSA or ECDSA
* These should be used for authorization or information exchange
* They consist of three parts header.payload.signature

## bcrypt docs
* npm install bcrypt
* hashes a password
* async mode is recommended