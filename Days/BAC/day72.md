# **Lab 6: Method-based access control can be circumvented**

This lab implements [access controls](https://portswigger.net/web-security/access-control) based partly on the HTTP method of requests. You can familiarize yourself with the admin panel by logging in using the credentials `administrator:admin`.

To solve the lab, log in using the credentials `wiener:peter` and exploit the flawed access controls to promote yourself to become an administrator.

---

Target Goal - Promote user to become administrator

first we are going to log in using the admin account and learn how the functionality work and then after we learn how the functionality is work, we are going to try to exploit it from our regular account user.

---

If we click on admin panel after we logged on admin user, you could see there is a functionality that can upgrade and downgrade user role. 

```html
POST /admin-roles HTTP/2
Host: 0a5f001f0469750fc246125e00cc0094.web-security-academy.net
Cookie: session=CUQ4wX5U6jFnbBUWUrAUyWZBJXQxfYBD

username=wiener&action=upgrade
```

So, now it looks good we know how the it function. now let’s go and logged out and log in in normal user.

---

If we try to do like an admin privileged user we can’t. But if this implemented incorrectly which means the access control implemented only in specific methods such us POST method but it’s not implemented on GET method… there is BUG! 

---

## **Solution💡**

1. Log in using the admin credentials.
2. Browse to the admin panel, promote `carlos`, and send the HTTP request to Burp Repeater.
3. Open a private/incognito browser window, and log in with the non-admin credentials.
4. Attempt to re-promote `carlos` with the non-admin user by copying that user's session cookie into the existing Burp Repeater request, and observe that the response says "Unauthorized".
5. Change the method from `POST` to `POSTX` and observe that the response changes to "missing parameter".
6. Convert the request to use the `GET` method by right-clicking and selecting "Change request method".
7. Change the username parameter to your username and resend the request.
