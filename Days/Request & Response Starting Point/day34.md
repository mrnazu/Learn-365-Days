# Request & Response

Starting point

# DNS

- **Domain Name System** aka **DNS**. It used to **match domain names with IP addresses**, so browsers can access websites trough DNS. It works by having a **distributed database of DNS records that matches domain names with their associated IP addresses.**
    - When you type a domain name into the search bar, such as `**nazu.com**`,your browser contacts it's DNS in order to translate the human-readable address into an IP address that computers use.
    
    ![what-is-a-dns-server.png](Request%20&%20Response%2002a6727f4d704b19bbfc3af3bf5d9e82/what-is-a-dns-server.png)
    

---

# HTTP Message

- **HTTP messages** are the **packages** it uses to move things around. HTTP messages are the blocks of data sent between HTTP applications. These blocks of data begin with some text meta-information describing the message contents and meaning, followed by optional data. These messages flow between clients, servers, and proxies.
- Meta-Information:
    
    ```
    GET/index.html HTTP/1.1 
    Host: www.nazu.com 
    Data:  
    <html><body><h1>Hi, welcome to Example!</h1></body></html>
    ```
    
    - In this example, the meta-information tells the HTTP application that this is a "**GET**" request for the file "index.html", using version 1.1 of the HTTP protocol. The data contains an HTML page with a friendly greeting. This message gets sent from the client to the server, which then returns it back to the original client or proxy in order to display it in a web browser.
    
    ## Message Syntax
    
    - All HTTP messages fall into two types: request messages and response messages. Request messages request an action from a web server. Response messages carry results of a request back to a client. Both request and response messages have the same basic message structure.
    
    ```
    # Request
    <method> <request-URL> <version>
    <headers>
    <entity-body>
    ======================================
    # Response
    <version> <status> <reason-phrase>
    <headers>
    <entity-body>
    ```
    
    ## HTTP Start Line
    
    All HTTP messages begin with a start line.
    
    ### Request line
    
    - Request messages ask servers to do something to a resource. The start line for a request message, or request line, contains a method describing what operation the server should perform and a request URL describing the resource on which to perform the method. The request line also includes an HTTP version which tells the server what dialect of HTTP the client is speaking.
    
    ### Response line
    
    - Response messages carry status information and any resulting data from an operation back to a client. The start line for a response message, or response line, contains the HTTP version that the response message is using, a numeric status code, and a textual reason phrase describing the status of the operation.
    
    ### HTTP Methods
    
    - The method begins the start line of requests, in short methods are the type of actions an HTTP request can take. Common examples include GET, PUT, POST, and DELETE. Each method has a different purpose and use case.
    - **GET** and **HEAD** Methods are said to be safe, meaning that no action by a An HTTP request that uses the GET or HEAD method. that means nothing will happen to the server with any action.
        - For example, consider when you are shopping online at Joe’s Hard-ware and you click on the “submit purchase” button. Clicking on the button submits a POST request with your credit card information, and an action is performed on the server on your behalf. In this case, the action is your credit card being charged for your purchase.
    - **GET**
        - GET is the most common method. It usually is used to ask a server to send a resource. or used to retrieve data from a specified resource. A simple example of a GET request is entering a URL into your web browser, your browser then sends a GET request to the server hosting that website and the server returns the requested resource to you.
        - Here's an example of how this works: writing "`www.nazu.com`" in your address bar can be thought of as sending an HTTP GET request for the file at `http://www.nazu.com/index.html` . The web server at `www.example.com` receives your request, looks up the requested file, and sends it back to you along with additional information about how to display it properly in your web browser, such as content type.
    - **HEAD**
        - HEAD requests are similar to GET requests; they retrieve resource content with the exception that t**hey do not retrieve the actual body of the resource**. Therefore, HEAD responses include all headers, including Content-Type, Content-Length and anything else that might be included with a GET request response - except its body content.
        
        ```
        Request: 
        HEAD /images/example.jpg HTTP/1.1
        Host: www.nazu.com
        ===============================
        Response: 
        HTTP/1.1 200 OK    (indicating status code) 
        Content-Type: image/jpeg     (showing type of data returned)  
        Content-Length: 5425821     (showing size of file returned in bytes)
        ```
        
    - **PUT**
        - The PUT method in HTTP requests can be used to create or update existing resources on the server.
        
        ```
        PUT http://www.nazu.com/api/book/1 
        Content-Type: application/json 
        Accept: application/json 
        {  
           "id": 1, 
           "author": "sam",   
           "title": "My First Book",  
           "publisher": "name of Publishing" 
        }
        ```
        
    - **POST**
        - A POST request is used when you need to send **data** to a server, for example, file upload, form data, etc. It is often used when submitting an HTML form.
    - **TRACE**
        - When a client makes a request, that request may have to travel through firewalls, proxies, gateways, or other applications. Each of these has the opportunity to modify the original HTTP request. The TRACE method allows clients to see how its request looks when it finally makes it to the server.
        - Which means in short it used to send client's request message and back to the client, identically. It can be used for debugging web applications and circumvent cross-site scripting (XSS) attacks.
        
        ![trace.png](Request%20&%20Response%2002a6727f4d704b19bbfc3af3bf5d9e82/trace.png)
        
    - **OPTION**
        - The OPTIONS method asks the server to tell us about the various supported capabilities of the web server. You can ask a server about what methods it supports in general or for particular resources.
        
        ```
        curl -X OPTIONS http://nazu.com/api/orders 
        HTTP/1.1 200 OK 
        Allow: GET,POST,HEAD,OPTIONS
        ```
        
    - **DELETE**
        - DELETE is used to request the server to delete a specified resource.
        
        ```
        DELETE /files/report.pdf HTTP/1.1 
        Host: nazu.com 
        
        Response: 
        HTTP/1.1 200 OK 
        Content-Type: application/json; charset=utf-8 
        {"message": "Successfully deleted report.pdf"}
        ```
        

## Status Codes

HTTP status codes are three-digit numbers that indicate how a server is responding to a client’s request. and HTTP status codes are classified into five broad categories.

1. **100–199: Informational Status Codes**
    1. HTTP/1.1 introduced the informational status codes to the protocol.
        1. **Clients and 100 Continue**
            1. If a client is sending an entity to a server and is willing to wait for a 100 Continue response before it sends the entity, the client needs to send an Expect request header. because this will only confuse the server into thinking that the client might be sending an entity.
        2. **Servers and 100 Continue**
            1. If a server receives a request with the Expect header and 100-continue value, it should respond with either the 100 Continue response or an error code. Servers should never send a 100 Continue status code to clients that do not send the 100-continue expectation.
        3. **Proxies and 100 Continue**
            1. A proxy that receives from a client a request that contains the 100-continue expectation needs to do a few things. If a proxy decides to include an Expect header and 100-continue value in its request on behalf of a client that is compliant with HTTP/1.0 or earlier, it should not for- ward the 100 Continue response (if it receives one from the server) to the client, because the client won’t know what to make of it.
2. 200–299: Success Status Codes
    1. When clients make requests, the requests usually are successful. in short Success status codes indicate that a server accepted and processed a request successfully.
3. 300–399: Redirection Status Codes
    1. The redirection status codes either tell clients to use alternate locations for the resources they’re interested in or provide an alternate response instead of the content. in short HTTP status codes that indicate whether a web page has moved permanently, temporarily, or is accessible under different URLs.
4. 400–499: Client Error Status Codes
    1. Sometimes a client (hackers) sends something that a server just can’t handle, such as a badly formed request message or, most often, a request for a URL that does not exist. We’ve all seen the infamous 404 Not Found error code while browsing this is just the server telling us that we have requested a resource about which it knows nothing. in short word HTTP Client Error Status Codes (4xx) are used for for errors that are caused by the client and indicate an error in the user's request.
5. 500–599: Server Error Status Codes
    1. Sometimes a client sends a valid request, but the server itself has an error. or in short HTTP Server Error Status Codes are 5xx-level status codes that indicate a server-side error. Common HTTP Server Error Status Codes include 500 Internal Server Error, 501 Not Implemented, 502 Bad Gateway, 503 Service Unavailable, and 504 Gateway Timeout.

## Headers

Headers and methods work together to determine what clients and servers do. which is very interesting part for hackers. or in short word HTTP headers are name and value pairs that form part of the header section of an HTTP request or response. They provide information about a particular transaction between the client and server, such as details about the requester, information about the content requested, the type of data being sent or received, authentication information, and more.

- **General headers**
    - These are generic headers used by both clients and servers. They serve general purposes that are useful for clients, servers, and other applications to supply to one another. in short HTTP general headers are used to send additional information in a response from a server to the client or to send additional information in a request from a client to the server. They provide control over how content is exchanged between parties.
        - Cache-Control - a directive setting caching parameters for resources that should be cached by the browser
        - Date - indicating when something was created, last modified, or generated;
- **Request Headers**
    - Request headers are specific to request messages. They provide extra information to servers, such as what type of data the client is willing to receive.
        - For example, the following Accept header tells the server that the client will accept any media type that matches its request: `Accept: **/**`
        - User-Agent - Tells the server the name of the application making the request
    - **Request security headers**
        - HTTP natively supports a simple challenge/response authentication scheme for requests. It attempts to make transactions slightly more secure by requiring clients to authenticate themselves before getting access to certain resources.
            - **Authorization** - Contains the data the client is supplying to the server to authenticate itself
            - **Cookie** - Used by clients to pass a token to the server—not a true security header, but it does have security implications
- **Response headers**
    - Response messages have their own set of headers that provide information to the client. for example what type of server the client is talking to: `Server: Apache/5.0`
- **Entity headers**
    - HTTP Entity headers are the part of a response from an HTTP server that provide information regarding the type, length, and encoding of the returned data. They are also used to control caching, compression and other types of content processing related to HTTP responses.
    - For example, the following Content-Type header lets the application know that the data is an HTML document in the iso-latin-1 character set: `Content-Type: text/html; charset=iso-latin-1`
    
    [](http://www.w3.org/Protocols/rfc2616/rfc2616.txt)
    

# HTTP Proxy

- HTTP Proxy is an intermediary between a client and a server, responsible for forwarding requests between two or more nodes. It allows clients to make indirect network connections to other network services. An HTTP proxy can be used to improve performance by caching commonly requested web pages on the server-side, allowing faster responses when the same content is requested again.
- For example, if a company uses an HTTP proxy server instead of making direct connections to websites, then any data requests would first go through the proxy server before it reaches the website's host computer. The response time will be reduced due to the local caching mechanism of the proxy. Furthermore, because all requests are routed through the same address, it provides better privacy as compared to directly connecting to websites without using a proxy - making it difficult to pinpoint individual traffic sources.

![proxy.png](Request%20&%20Response%2002a6727f4d704b19bbfc3af3bf5d9e82/proxy.png)