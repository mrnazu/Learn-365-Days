# AuthN & AuthZ

# What is Authentication

- Web app authentication is the process of verifying the identity of a user who is attempting to access a web application. This process typically involves the user providing a username and password, which is then compared against a database of authorized users. If the credentials match, the user is granted access to the application. Other forms of authentication may include biometric authentication, two-factor authentication, or single sign-on (SSO).
- For example, when you log into an online banking website, you are asked to enter your username and password. This is an example of authentication, as the website verifies your identity before allowing you access to your account.

# What is Authorization

- Web authorization is the process of granting access to a website or web application based on a user's identity. It is used to control who can access certain resources and what they can do with them
- For example, when you log into an online banking website, the website will use web authorization to verify your identity and grant you access to your account. Once you are logged in, you will be able to view your account information, transfer funds, changing profile and more.

# Authorization vs Authentication

- Authentication is the process of verifying the identity of a user or device. It is typically done by requiring a username and password, or by using biometric data such as fingerprints or facial recognition.
- Authorization is the process of determining whether an authenticated user has permission to access a particular resource. It involves granting access to certain resources based on the user's identity and privileges.
    - For example, a user may be authorized to view certain files but not edit them.

---

# Multi-Factor Authentication

- Multi-Factor Authentication (MFA) is an authentication method that requires more than one form of authentication to verify a user's identity. Examples of MFA include using a combination of something you know (like a password), something you have (like a security token or mobile device), and something you are (like biometric data).
- For example, when logging into an online banking account, the user may be required to enter their username and password, as well as provide a one-time code sent to their mobile device.
    - An example of multi-factor authentication in the real world is using a bank card to withdraw money from an ATM. The user must provide two factors of authentication: something they know (their PIN) and something they have (their bank card).

# Access Control

- Web app Access Control is a security measure that restricts access to certain parts of a web application based on user roles and permissions. It is used to ensure that only authorized users can access sensitive data or perform certain actions.
- A real world example of web app Access Control would be an online banking system. The system would restrict access to certain features, such as transferring funds, based on the user's role and permissions.
    - For example, a regular user may only be able to view their account balance, while an administrator may have the ability to transfer funds between accounts.

# OTP

- OTP stands for One-Time Password. It is a unique, randomly generated code that is used to authenticate a user for a single transaction or session. OTPs are typically sent via SMS or email and are used as an additional layer of security when logging into an account
- For example, when you log into your online banking account, you may be asked to enter an OTP that was sent to your mobile phone. This ensures that only you have access to your account and prevents unauthorized access.

# Encryption and Digital Signatures

- Encryption is a way of scrambling data so that only people with the right key can read it. It's like a secret code that only you and the person you're sending the message to can understand.
- Digital signatures are like a digital version of your signature. They are used to prove that a document or message came from you and was not changed in any way. It's like signing your name on a paper document, but instead of using ink, you use a special code that only you know.
- A real world example would be sending an email to their teacher. Encryption would be like writing the email in secret code so that only their teacher can read it. Digital signatures would be like signing their name at the bottom of the email so their teacher knows it really came from them and wasn't changed by anyone else.

---

# Implementation

- Authentication and authorization are two important security concepts that are used to protect data and resources. Authentication is the process of verifying the identity of a user or system, while authorization is the process of granting access to resources based on the user's identity.
- Authentication:
    - Authentication is typically done through a username and password combination, but can also be done using biometric data such as fingerprints or retinal scans. The authentication process typically involves comparing the credentials provided by the user with those stored in a database. If they match, then the user is authenticated and allowed access to the system or resource.
- Authorization:
    - Once a user has been authenticated, authorization can be used to determine what level of access they have to certain resources. This is usually done by assigning roles or permissions to users that define what they can do within the system.
        - For example, an administrator may have full access to all resources while a regular user may only have access to certain parts of the system. Authorization also helps ensure that users only have access to resources that they are authorized for, preventing unauthorized access or misuse of sensitive data.

---