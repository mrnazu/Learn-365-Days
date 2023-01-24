Cross-Origin Resource Sharing aka CORS

🛑 Cross-origin resource sharing aka #CORS is an important security header that defines how web browsers, web servers, and other web applications interact with each other across domains. in short word cross-origin resource sharing or cores is a mechanism that allows a website on one url to request data from a different url.

🛑 To understand CORS better, let's look at an example of a request to a website www.nazu.com with a domain of the same name. Without CORS in place, the browser automatically blocks all requests from any other domain associated with www.nazu.com except for its own domain because this is considered to be a cross-origin request. 

🛑 The most basic example of CORS is when a web page attempts to access content from a different origin (domain, protocol, or port). In that case, the browser must first issue an HTTP request with an Origin header indicating the requesting origin.

🛑 The server can then respond with an Access-Control-Allow-Origin header indicating which origins can access that content. This enables web pages on one domain to access data from another domain in a secure manner. Here's an example of a CORS request:

Request: 
```
GET /resource HTTP/1.1 
Host: nazu.com 
Origin: http://website.com
```
Response: 
```
HTTP/1.1 200 OK 
Access-Control-Allow-Origin: http://website.com
```
👥Group @mrnazuu
📢 Channel @mrnazu

✍️Written by Nazu

                💀@mrnazu💀
             #Knowledge_Is_Free 
          #share_and_support_us

#cors #header #http #bugbounty #url
