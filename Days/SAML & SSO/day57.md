# SAML

# **What is SAML**

Security Assertion Markup Language aka SAML, often pronounced as "sam-el") is an open standard for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider. It is commonly used as a means of allowing single sign-on (SSO) access to web applications.

Real world example: Consider that you are working for an organization with multiple customer sites all spread over different countries and many external contractors who are allowed access to the network. With SAML you can easily create a secure single sign-on system, by which the organization can grant access rights to anyone who needs it without having to set up separate user accounts for each person or site. This helps provide a secure way of authenticating users, regardless of their location or device, protecting both your customer’s private information and your company's security.

![saml-flow-citrix.png](SAML%209e028e91f21b4229b05b3505733c78cb/saml-flow-citrix.png)

---

# How it Works

For example, if a user wanted to access a service offered by a service provider (e.g. Salesforce), the user could authenticate himself via an external authentication system, such as Active Directory Federation Services (ADFS). After a successful authentication, ADFS would issue an XML-encoded SAML assertion containing the users' identification and attributes like name or Role Group membership, to renew access to Salesforce. The SAML assertion is digitally signed so that the identity of both the parties and integrity of the message can be verified by any validating party.

Salesforce then needs to validate this SAML assertion so it can authenticate the user and grant him access to its services. To do this, Salesforce verifies the signature on the SAML assertion using certificates provided by ADFS beforehand and authenticates the user upon receipt of a valid response. If all is successful, Salesforce will create a session for that particular user enabling him access typical services like creating documents or changing settings within his account.

---

# **SAML Benefits**

1. Increased Security: SAML enables strong authentication through the exchange of digitally signed XML documents, providing improved security over logins based on plain text passwords. This technology provides an extra layer of protection against unauthorized access and reduces the risk of system infiltration.
2. Reduced Dependence on Passwords: Passwords can be difficult to remember, especially for complex website logins, which makes them vulnerable to hacking attempts. With SAML you no longer have to rely on a user’s ability to remember their password as it is replaced with stronger authentication factors such as digital certificates or biometrics authentication.
3. Cost Efficiency: With a centralised system such as SAML single sign-on (SSO), organisations no longer need to invest in user management systems or carry out regular manual maintenance tasks such as password resets or account provisioning processes, which leads to cost savings in terms of both time and money.
4. Easy Deployment: As there are no software programs that need to be installed across multiple devices, it makes the deployment of SAML SSO solutions quick and easy for organisations scaling up their IT infrastructure across multiple locations or services.
5. Accessibility Across Multiple Platforms: SSO has been used for some time now with many applications like email services and social networking sites using its advantages for users who wish to access their accounts from different platforms (example desktop computer, tablet). Now thanks to SAML, this same level of accessibility is available across even more web services and applications with ease without relying on numerous usernames/passwords combinations

---

# Real World SAML

The following example is a real-world scenario where SAML is used.

Suppose Company A, which uses an on-premises identity provider (IdP), purchases software services from Company B, which has its own cloud-based service. Company B needs to authenticate their customers when they access their services and discover the identity of the users requesting for the services. The companies will use SAML to enable secure authentication and authorization between them.

Company A will act as an IdP, or Service Provider (SP), in this particular case. When a user from Company A attempts to log into Company B's cloud-based platform, the user will enter their credentials into Company A's IdP system. If authenticated, the IdP will generate a SAML assertion with details about the user like their name, email address etc., and encrypts it with a shared secret key known only to both parties. Company B's service provider (SP) can then use the encrypted message to verify that they are receiving the data from a trusted source and authenticates the user based on the information provided in the SAML assertion. The user is then allowed access to the platform with appropriate authorization privileges.

# **What is SSO?**

Single Sign-On (SSO) is an authentication mechanism that allows users to log in with a single set of credentials to access multiple applications. 

For example, Google and Microsoft both allow users to log in with a single set of credentials, which can then be used to access multiple services such as Gmail, YouTube, Office 365, etc. By using SSO, users do not have to remember different passwords and usernames for different applications.

# Difference between SSO & SAML

Single sign-on (SSO) is an authentication process that allows a user to access multiple applications with one set of credentials. It is a common method used in enterprise systems to streamline the user experience.

Security Assertion Markup Language (SAML) is an XML-based open standard data format for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider. SAML is often used together with SSO and provides the technical foundation for allowing SSO to be securely implemented.

---