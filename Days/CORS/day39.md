# CORS

# What is CORS

- Cross-Origin Resource Sharing aka CORS s an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources.
- For example, a web page served from `https://nazu-a.com` can make a request for an image served from `https://nazu-b.com`. CORS defines a way in which the browser and server can interact to determine whether or not to allow the cross-origin request.
- In order to enable CORS, the server at `otherdomain.com` must include the following HTTP header in its response:
    - Access-Control-Allow-Origin: `http://example.com`

![cors.png](CORS%204e921c2d991f4bd78d0c2b5bb0a2ca90/cors.png)

---

## **Same-origin policy**

- The same-origin policy is a critical security mechanism that restricts how a document or script loaded by one origin can interact with a resource from another origin.
- For example, `http://www.nazu.com/script` is the same origin as `http://www.example.com/css` but not `https://www.nazu.com/css` because the scheme is different. that means if a website at `http://nazu.com` contains a script that attempts to access data from `http://evilhacker.com`, the Same-origin policy will prevent the script from accessing the data. This is because the two websites have different origins (`nazu.com` and `evilhacker.com`).
- It prevents a malicious website from accessing data from another website, such as cookies, session tokens, or other sensitive information. The policy works by comparing the origin of the requesting website to the origin of the resource being requested. If they match, then the request is allowed; if not, then it is blocked. This helps protect users from malicious websites that may try to steal their data or hijack their sessions.

![Same-Origin-Policy-restrictions-2.png](CORS%204e921c2d991f4bd78d0c2b5bb0a2ca90/Same-Origin-Policy-restrictions-2.png)

---

# Explain for kid

- CORS
    - CORS is a way for websites to share resources with each other. It allows websites to access data from other websites, even if they are on different servers. This means that a website can use images, videos, and other content from another website without having to copy it onto their own server.
- SOP
    - The Same-origin policy (SOP) is a rule that helps keep your information safe when you're using the internet. It means that websites can only access information from other websites if they are from the same origin. For example, if you're on a website called `www.example.com`, it can only access information from other websites that also start with `www.example.com`. This helps protect your personal information and keeps it safe from being accessed by other websites.

---

# Real world CORS Example

- A real world example of CORS is when a website such as `Amazon.com` wants to allow other websites to access its data.
- For example, if a third-party website wants to access Amazon's product information, they can use CORS to make an HTTP request from their own domain and receive the data from Amazon. This allows the third-party website to display the product information on their own site without having to host it themselves.

![real world.png](CORS%204e921c2d991f4bd78d0c2b5bb0a2ca90/real_world.png)