# API

**API** stands for **Application Programming Interface**. APIs allow one application to communicate with another without having to have direct interoperability mechanisms built within. IOW APIs allows two applications to talk to each other**.** APIs are used to integrate new applications with existing software systems.

A good example of an **API** is the **Google Maps** API. This allows developers to embed Google Maps into their websites and applications. The Google Maps API defines how developers can access and use the map data provided by Google. It also defines how developers can add their own custom features to the map, such as adding markers or custom overlays IOW MR **Y** can **communicate** and use the all **data** of MR **X** via their API.

# API Architecture

- **REST API**
    
    API Architecture is a set of rules and standards that define how an API should be **structured**, **designed**, and **used**. It’s a way of organizing the components of an API so that it can be easily understood and used by developers. and REST APIs are stateless.
    
    A good example of API Architecture is the Representational State Transfer aka REST. REST is an architectural style for designing distributed systems that use **HTTP** as the communication protocol. and it’s easy to **use**. REST APIs are organized into resources, which are accessed using HTTP **methods** such as **GET, POST, PUT, and DELETE**. Each resource has its own URL which can be used to access it. They are often used for **web-based applications** and **mobile applications**. 
    
    An example of a REST API is the **Twitter** API, which allows developers to access certain parts of the Twitter platform such as user profiles and maybe tweets using HTTP requests.
    
- **SOAP API**
    
    **SOAP** stands for **Simple Object Access Protocol,** and it’s not an architecture, it is a **protocol.** and its **Extensible Markup Language aka XML.**  SOAP uses SSL also **REST API** use SSL as well. SSL stands for Secure Sockets Layer, and is a security protocol used to encrypt data. 
    
    A best example of SOAP API would be a web service that provides weather information. The client application sends an **XML** **request** to the server, which contains information such as city name, zip code, etc. The server then processes the request and sends back an **XML** **response** containing the weather information for the specified location. The client application can then parse this response and display it in a user-friendly format.
    

# Types of API - 3

- **Open API**
    
    aka public APIs, these are freely available for developers and it can be used without any restrictions or authentication to access the API or its resources.
    
- **Partner API**
    
    These are APIs that are provided by a partner company or organization and require some form of authentication or agreement before they can be used.
    
- **Internal API**
    
    Require Authentication and they are not exposed to the public. They are typically used for internal applications or services.
    

# API Pen-Testing - Security

API pen-testing is a type of security testing that focuses on testing the security of an API. For example, a pen-tester might send a request with malicious code to trick or in order to see if the API can be exploited.

# OWASP API Top 10

OWASP API Top 10 is a list of the top 10 most critical security risks to APIs. It was created by the Open Web Application Security Project aka OWASP.

- Broken Object Level Authorization
- Broken User Authentication
- Excessive Data Exposure
- Lack Of Rate Limiting
- Broken Function Level Authorization
- Mass Assignment
- Security Misconfiguration
- Injection
- Improper Assets Management
- Insufficient Logging & Monitoring
