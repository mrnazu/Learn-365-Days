# **Lab 3: User role controlled by request parameter**

This lab has an admin panel at `/admin`, which identifies administrators using a forgeable cookie.

Solve the lab by accessing the admin panel and using it to delete the user `carlos`.

You can log in to your own account using the following credentials: `wiener:peter`

---

So, when we say “Forgeable cookie” what it mean? well, Forgeable Cookie aka Forged Cookie is a cookie created maliciously to pretend to be someone else. This happens without the person knowing their password.

Example: A hacker can create a forged cookie that appears as someone else's valid cookie, and use it to gain access to the person's account information.

---

## **Solution💡**

1. Browse to `/admin` and observe that you can't access the admin panel.
2. Browse to the login page.
3. In Burp Proxy or in Cookie extension, turn interception on and enable response interception.
4. Complete and submit the login page, and forward the resulting request in Burp.
5. Observe that the response sets the cookie `Admin=false`. Change it to `Admin=true`.
6. Load the admin panel and delete `carlos`.
