# Bearer Authentication

## Intro to JWT

1. **What is a JSON Web Token (JWT)?**
   - JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

2. **When should we use JSON Web Tokens?**
   - JWTs are useful in the following scenarios:
     - **Authorization:** Once a user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT because of its small overhead and its ability to be easily used across different domains.
     - **Information Exchange:** JWTs are a good way of securely transmitting information between parties. They can be signed to ensure the sender's authenticity and to verify that the content hasn't been altered.

3. **Claims are expected in which structural component of a JWT?**
   - Claims are expected in the **Payload** component of a JWT.

## Are JWTs Secure? 

1. If I get a JWT and I can decode the payload, how can we call that secure?

    JWTs are not meant to hide or encrypt data; rather, they ensure the integrity of the data. When we say a JWT is secure, we mean that once it's signed, you can't tamper with its content without invalidating its signature. The payload of a JWT is merely encoded in Base64 format, which can be easily decoded. The real security comes from the signature, which is created using a secret key. If someone alters the payload, the signature will no longer match, indicating potential tampering. 

2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.

    When sending a JWT, both the sender and the receiver must know the secret (or in the case of public/private key pairs, the private key for the sender and the public key for the receiver). Thsi secret is used to create the JWT's signature on the sender's side and to verify the JWT's signature on the receiver's side. The signature ensures the token's intregrity and authenticy. 

3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.

    Imagine you're sending a sealed letter through the mail. The content of the letter is like the payload of a JWT, and the seal on the envelope is like the signature. The seal is made using special wax that only you and the recipient know about. When the recipient gets the letter, they can easily open it and read the content. However, if someone tried to tamper with the letter in transit, the seal would break, and the recipient would know the letter might have been tampered with. Similarly, with JWTs, the content (or payload) is easily readable, but the signature (or seal) ensures that it hasn't been tampered with during transit. 

## JWTs Explained 

1. Why use JWT?

   JWT (JSON Web Token) is used because it offers a secure and efficient method for representing claims between two parties. It's especially beneficial in authentication and authorization protocols. The token can contain all the necessary information about a user, which means systems don't have to repeatedly query databases to fetch user details. This makes processes like user authentication faster and more efficient. Additionally, JWTs can be digitally signed, ensuring the integrity and authenticity of the information they carry.

2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.

   Imagine you have a small suitcase (JWT) that you can easily carry with you on a plane without checking it in. Inside this suitcase, you have everything you need for your trip (user information). Because it's compact, it's easy to take with you wherever you go (transmitted through URLs, POST parameters, or HTTP headers). And since it's self-contained, you don't need to keep opening other bags (querying databases) to get what you need. This makes your journey (web processes) faster and smoother.

3. What are the three components (the structure) of a JWT signature?

   - **Header**: This part specifies the type of the token (which is JWT) and the algorithm used for signing, like HMAC SHA256 or RSA.
   - **Payload**: This section contains the claims, which are statements about an entity (usually the user) and additional data.
   - **Signature**: This is created by taking the encoded header and the encoded payload, then using a secret and the algorithm specified in the header to sign them. The signature ensures the token hasn't been tampered with and verifies its authenticity.

## Things I want to know more about:

While I've gained a foundational understanding of JWTs, there are still areas I'd like to delve deeper into:

- **Token Expiry and Refresh**: How do systems handle token expiration and what's the process for refreshing a token? How does this ensure continued security?
- **Best Practices**: What are the best practices for storing and transmitting JWTs to ensure maximum security? I've heard about potential vulnerabilities like token leakage; how can these be prevented?
- **Advanced Use Cases**: Beyond authentication and authorization, are there other advanced use cases for JWTs in modern web applications or other platforms?
- **Alternatives to JWT**: While JWT seems to be a popular choice, are there other token-based authentication methods that might be more suitable for certain scenarios or that offer different advantages?
- **Public/Private Key Pairs**: I understand the basic concept, but how does the process of using public/private key pairs with JWTs work in real-world applications? How do systems ensure the private key remains confidential?

These are areas I believe would provide a more comprehensive understanding of JWTs and their application in various scenarios.

#### Citations
- [Introduction to JSON Web Tokens](https://jwt.io/introduction/)
- [If you can decode JWT, how are they secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
- [What is JWT? JSON Web Token Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
