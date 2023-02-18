# OAuth Access Token

# What is OAuth Access Token

- OAuth Access Token is a type of token used in OAuth 2.0 authentication protocol. It is a string of characters that represents an authorization granted by a user to an application. The access token is used to authenticate the user and authorize the application to access the user's data.
- For example, when a user logs into an application using their Google account, they are asked to grant permission for the application to access their Google data. If they agree, Google will generate an OAuth Access Token that can be used by the application to access the user's data.

---

# How it is used

- Let's say you are using an app that requires you to log in with your Google account. When you enter your credentials, the app sends a request to Google's OAuth server for an access token. The server then verifies your credentials and sends back an access token that the app can use to make API calls on your behalf. The access token is then stored in the app and used for all subsequent requests until it expires or is revoked by the user.

---

## Single Sign-On (SSO)

- Single Sign-On (SSO) is an authentication process that allows a user to access multiple applications or websites with one set of credentials.
- For example, if a user logs into their Google account, they can access Gmail, Google Drive, and other Google services without having to log in again. This saves time and makes it easier for users to access the services they need.

---

# User Identity Delegation

- User Identity Delegation is a security feature that allows users to access resources on behalf of another user. It is commonly used in enterprise environments where users need to access resources that are owned by other users.
- For example, a system administrator may need to access files owned by other users in order to perform maintenance tasks. In this case, the system administrator can use User Identity Delegation to temporarily assume the identity of the other user and gain access to their files.

---

## Token

- A token is a piece of data that is used to identify a user or application in an authentication process. It is typically generated by the server and sent to the client when the user logs in.
- For example, when a user logs into a web application, the server may generate a token and send it to the client. The client can then use this token to authenticate itself with the server for us.

# Bearer Token

- A Bearer Token is an access token that is issued to a client by an authorization server. It is used to authenticate the client when making requests to protected resources
- A real world example of a Bearer Token would be a security token that is issued by a bank when you log in to your online banking account. The token allows the bank to verify your identity and grant you access to your account information.

## Macaroon Token

- Macaroon tokens are a type of token-based authentication that uses a hierarchical structure to provide access control. They are typically used for authorization in distributed systems, and are composed of three parts: the identifier, the caveats, and the signature.
- Bearer tokens are a type of token-based authentication that is sent in an HTTP Authorization header. They are typically used for authentication in web applications, and consist of a string of characters that represent the user's identity.

---

# Hash Token

- A hash token is a unique string of characters that is used to identify a user or transaction. It is generated by applying a cryptographic hash function to some data, such as a username, password, or other information.
- For example, when you log into an online banking system, the system may generate a hash token based on your username and password. This token is then used to authenticate your identity and authorize access to the system.

---

# JWT Token

- JWT (JSON Web Token) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. It is typically used to transmit information that can be verified and trusted by both parties, such as authentication and authorization data.
- For example, when a user logs into an application, the application can generate a JWT token containing the user's identity and other relevant information. The application then sends this token to the user's browser, which stores it in local storage. When the user makes subsequent requests to the application, they include this token in their request header. The application can then use the token to verify the user's identity and authorize them to access certain resources or perform certain actions.

---

# Implementation of Access Token

- An access token is a type of credential that is used to gain access to a secure system. It is typically issued by an authentication server and contains information about the user, such as their identity, privileges, and other claims. Access tokens are commonly used in web applications and APIs to authenticate users and authorize their access to resources.
- Alice wants to access her bank account online. She logs into the bank's website with her username and password. The bank's authentication server then issues an access token for Alice that contains her identity and other claims about her privileges. The token is then sent back to Alice's browser, which sends it along with each request she makes for a resource from the bank's website or API. The bank's server verifies the token before granting Alice access to the requested resource.