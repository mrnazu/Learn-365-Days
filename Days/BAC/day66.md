# BAC 3| How to Find Access Control Vulnerabilities?

Access control vulnerabilities are among the most common and dangerous security flaws in web apps. These vulnerabilities can allow attackers to gain unauthorized access to sensitive data or perform other malicious actions. Here are some ways to find access control vulnerabilities:

1. Conduct a Security Audit: A comprehensive security audit is the best way to identify access control vulnerabilities. This process involves identifying all access points to the system, ensuring that the access controls are properly configured, and testing the system for vulnerabilities.
2. Use Automated Scanners: Automated scanners can be used to identify common access control vulnerabilities, such as weak passwords, missing access controls, and misconfigured permissions.
3. Conduct Manual Testing: Manual testing involves examining the system's access controls in detail, looking for weaknesses or misconfigurations that may not be detected by automated scanners. This approach requires more time and expertise but can be more effective in identifying complex vulnerabilities.
4. Analyze Code: Analyzing the code of the system can help identify access control vulnerabilities that might not be visible through other means. This approach requires a deep understanding of the system architecture and coding practices.
5. Use Penetration Testing: Penetration testing involves simulating an attack on the system to identify potential vulnerabilities. It can be a useful way to identify access control vulnerabilities that might not be detected through other methods.

Examples of access control vulnerabilities include weak passwords, missing access controls, misconfigured permissions, and broken session management. These vulnerabilities can be exploited by attackers to gain unauthorized access to sensitive data or perform other malicious actions, such as modifying or deleting data, stealing sensitive information, or launching further attacks. It is important to regularly test for access control vulnerabilities and implement appropriate security measures to prevent them.

# How to Exploit Access Control Vulnerabilities?

- depends on the types of access control vulnerability
- vulnerable fields and parameters

# Access Control Examples

- Bypassing access control checks by modifying parameters in the URL or
HTML page.
- Accessing the API with missing access controls on the POST, PUT and
DELETE methods.
- Manipulating metadata, such as replaying or tampering with JSON Web
Tokens (JWTs) or a cookie.
- Exploiting CORS misconfiguration that allow API access from unauthorized /
untrusted origins.
- Force browsing to authenticated pages as an unauthenticated user.
