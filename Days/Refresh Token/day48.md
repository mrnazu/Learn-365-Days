# Refresh Token

# What is Refresh Tokens

- Refresh tokens are a type of token used to obtain a renewed access token. They are typically used in applications that use OAuth 2.0 for authentication and authorization. or in short A refresh token is a special key that enables a client for an API or service to retrieve new access tokens without requiring the user to perform a complete login. In other words, an application can exchange a valid refresh token for a new access token.
- A refresh token is a long string of characters that is sent to the client when the access token is granted. The client can then use the refresh token to get a new access token when the current one expires.
- For example, if you log into an application using your Google account, you may be asked to grant permission for the application to access certain information from your Google account. When you grant permission, Google will send an access token and a refresh token to the application. The application can then use the access token to make API calls on your behalf, and it can use the refresh token to get a new access token when the current one expires.

![How-a-refresh-token-is-generated-and-used-1.png](Refresh%20Token%20695b04d036744c0c9ce68fb8fdd601b0/How-a-refresh-token-is-generated-and-used-1.png)

---

# How Refresh Tokens work

- Refresh tokens are used to obtain a new access token without having to re-authenticate the user.
- A real world example of this would be when a user logs into an online banking application. After the user has successfully authenticated, they will be issued an access token that allows them to access their account information. This access token will expire after a certain amount of time, usually an hour or two. When the access token expires, the user can use their refresh token to obtain a new access token without having to re-authenticate. This allows the user to continue using the application without having to log in again.

---

# How They are used

- Refresh tokens are used to obtain a new access token without requiring the user to re-authenticate.

---

# Implementations

- JWT Refresh Token: A JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. It can be used as a refresh token to provide access to resources without requiring the user to re-authenticate.
- OAuth Refresh Token: OAuth is an open standard for authorization that provides a way for users to grant third-party applications access to their web resources without sharing their credentials. OAuth refresh tokens are used to obtain new access tokens when the existing access token has expired or become invalid.
- SAML Refresh Token: Security Assertion Markup Language (SAML) is an XML-based open standard data format for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider. SAML refresh tokens are used to obtain new SAML assertions when the existing assertion has expired or become invalid.

---

# Real World Example

- A refresh token example would be when a user logs into an online banking website. After the user logs in, they are given a refresh token that allows them to access their account without having to log in again. The refresh token is stored on the user's device and is used to authenticate the user when they return to the website. The refresh token is typically valid for a certain period of time, after which it must be renewed or replaced with a new one.

---

---