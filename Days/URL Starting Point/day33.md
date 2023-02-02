# URL Starting point

# URL

- **URL** stands for **Uniform Resource Locator,** that allows users to access **objects** on a **server**, such as web pages and other content. It can contain a variety of information such as the host name, port number, path, query parameters and more. as a wiki post A URL is a specific type of **Uniform Resource Identifier** aka **URI**, although many people use the two terms interchangeably.

![the-structure-of-a-url.png](URL%20712c8d5fb3884021a9c0abb23249a6aa/the-structure-of-a-url.png)

---

- To Explain this URL [`**https://nazu.com/test/file.php?id=12#](http://www.hackxpert.com/test/test.php?id=1245#nsksjhd)about**`
    - Protocol (**HTTP**) This is the protocol used for communication between the web server and the browser. In this case, it is Hypertext Transfer Protocol (HTTP)
    - Host Name ([`**nazu.com**`](http://www.hackxpert.com/)) The host name is the domain name and it identifies where a website is hosted on the Internet. It is like an IP address, but easier to remember for humans.
    - Path (**`/test/file.php`**) This part of a URL refers to a specific page or resource on a web server. In this case, it resolves to "/test/file.php", meaning that the browser requests a web file named "file.php" from a folder called "test".
    - Query Parameters (**`?id=12`**) A query parameter is additional information added to a URL after a question mark (**`?`**). It's usually used in dynamic websites to perform specific tasks, such as loading different versions of a page or sending search queries to websites. In this example, the query parameter passes an ID number - 12 - into the document being requested on the server.
    - Anchor Text (**`#about`**) The anchor text part of a URL comes after an #, and often holds information about which section of a web page should be brought into focus when it loads in your browser window from the web server (such as headers, images or text). In this example "**#about**" could signify that when requested, it brings with it additional information related to "about page or something".

## Parameters

- like i mentioned before  a query parameter is additional information added to a URL after a question mark. that are used to pass information between a client and a server. This technology is commonly used for passing form data, or for tracking session information such as user IDs, login names, and other variables. Parameters take the form of key-value pairs, with keys typically defined by the application sending the request and values populated by the user accessing a website.
    - `?name=nazu&age=100`
- As a security researcher, It's important to properly validate all HTTP URL parameters before processing them. cuz they can often contain data that may not be properly sanitized.

[URL - Wikipedia](https://en.wikipedia.org/wiki/URL)
