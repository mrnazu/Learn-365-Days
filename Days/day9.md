# SSRF in short

Server-side request forgery aka SSRF first described in 2008, A Server-Side Request Forgery attack involves an attacker sending a forged request, with malicious code, from the vulnerable server directly to another host in order to gain access to vulnerable web pages, ports and other sensitive data. The attacker does this by embedding malicious code into the target servers request and forcing it onto the intended host. 

For example, an attacker might use SSRF to locally file or database read of a system. lemm add another one: if a web app that allows users to make HTTP requests and has no input validation implemented, an attacker aka hunters is able to specify any URL they want in the request and could use this vulnerability to forward requests to internal systems not intended for public access.

To perform an SSRF attack, we will first identify which web applications are vulnerable and then craft malicious requests that are sent from those applications to systems or services running inside the target's network. The requests can include parameters such as IP addresses, host names, port numbers, overall URLs that allow for code execution or command injection attacks. Once these attacks are sent, the attacker can then attempt to take control of the system or collect confidential information.

- **To find and detect these SSRF vulnerabilities**
    - Look for user input being included in the URL or HTTP request body - If a user is able to provide data that is appended to a URL or included as part of an HTTP request body, this could potentially be manipulated by attackers to force their own requests.
    - Pay particular attention to any requests coming from “unusual” sources such as known internal IP ranges or local addresses which should not have access to external networks.
- **Preventing SSRF**
    - **Input Filtering**: Sanitize and filter user input, limiting to
    known good data inputs and Potential for regex data matching
    for validation
    - **Whitelisting**: Restrict access to internal resources using a specific whitelist of organizational domains. you can use regex

- **lemm more clear it**
    - If i make a request to a web server, it will return a 200 OK `GET /login` ⇒ `200 OK`
    - However, if i make request to the API server, i get a 403 forbidden cuz it's only accessible from the internal network or intranet also intranet is a type of internal network. `GET /api/v1/index/1` ⇒ 403 Forbidden
    - So I uploaded a profile picture to example website
    - Then i put the URL of the profile picture in the database. so this means the server will send request to URL and then fetch the image
    - Intercept the request and then Instead of it, we enter another URL. maybe `/api/v1/index/1` this means we are in the some network.

### Overall, **Example:**

- `POST /account/index HTTP/1.1
Content-Type: application/x-www-form-urlencoded
Host: example.com
Content-Length: 4321
url=example.com/account/edit.php`
- if i change the `url = example.com/account/edit.php` ⇒ [`localhost`](http://localhost)  or **Internal** ip boom we got access cuz it’s located behind a **firewall**. `url = 127.0.0.1`

[**SSRF Lab**](https://portswigger.net/web-security/all-labs#server-side-request-forgery-ssrf)
