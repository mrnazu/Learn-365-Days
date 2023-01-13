# **Information disclosure**

Information disclosure, also known as information leakage, is when a website unintentionally **reveals sensitive information** to its clients. Depending on the context, websites may leak all kinds of information to a potential attacker, **including**:

- Data about other users, such as usernames or financial information
- Sensitive commercial or business data
- Technical details about the website and its infrastructure

**Example**:

Let’s say an attacker is able to guess the URL of a restricted page on the website, such as [`https://example.com/data/secret-records.php](https://www.examplewebapp.com/data/secret-records.php).` If there are no proper **authentication** measures in place (for example, requiring users to log in via a **username** and **password** to view any content on the page) … then the attacker could view this confidential data without permission. Any data being stored from user inputs can then be easily obtained by the attacker if these measures aren't taken during development of the application.

# E**xploit ⇒ Portswigger lab**
