# ****Lab 5: URL-based access control can be circumvented****

This website has an unauthenticated admin panel at `/admin`, but a **front-end system** has been configured to block external access to that path. However, the back-end application is built on a framework that supports the `X-Original-URL` header.

To solve the lab, access the admin panel and delete the user `carlos`.

---

This means that any requests sent to the URL "/admin" from outside the system will be blocked, preventing unauthorized access to the secure parts of the system.

The X-Original-URL header is an HTTP response header which is set by servers that are using URL rewriting. This header contains the original URL a client has requested prior to being changed or rewritten by the server, while the location indicates to where it was rewritten.

In short that the X-Original-URL header is set by servers using URL rewriting. This header stores the original URL requested by a client, before being changed or rewritten by the server. The Location header indicates where the URL was rewritten to.

For example, imagine a user visits a website using their browser. The browser makes an HTTP request to the server and transmits an X-Original-URL with it containing the exact URL requested. The server then may forward that request to a CDN, which could also add an X-Original-URL to the request containing the same URL as before. When the CDN forwards the request back to the origin server, it would contain both headers - allowing for easier logging and tracking of requests for security purposes.

---

## **Solution💡**

1.  to load `/admin` and observe that you get blocked. Notice that the response is very plain, suggesting it may originate from a front-end system.
2. Send the request to Burp Repeater. Change the URL in the request line to `/` and add the HTTP header `X-Original-URL: /invalid`. Observe that the application returns a "not found" response. This indicates that the back-end system is processing the URL from the `X-Original-URL` header.
3. Change the value of the `X-Original-URL` header to `/admin`. Observe that you can now access the admin page.
4. To delete the user `carlos`, add `?username=carlos` to the real query string, and change the `X-Original-URL` path to `/admin/delete`.
