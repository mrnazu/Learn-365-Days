# Media Type - MIME

Starting point

# MIME - Multipurpose Internet Mail Extensions

- HTTP Media Type is a standard for specifying the type of data being sent or requested and response over the Internet. in short word it used to describe the contents of a HTTP message entity body, for both request and response. it called Multipurpose Internet Mail Extensions aka MIME type.
- image/gif – Graphics Interchange Format (GIF) images
- application/json – JavaScript Object Notation (JSON) Related Documents
- video/mp4 – MPEG4 Video Files

![mime.png](Media%20Type%20-%20MIME%2066ba9dcf2a1746ceaae244ec9bf80d10/mime.png)

- For example, a browser requesting an HTML file will use the MIME type **text/html**. This tells the server that it needs an HTML document and if it can't find one then it won't send anything. On the other hand, if a browser requests an image file like a JPEG or PNG, then it will use the appropriate MIME type such as image/jpeg or image/png in order to ensure that it receives the right type of file.
- Web Developers can also create custom MIME types for their needs. For example, if your website uses a custom log format, you could define a custom MIME type so that different devices can properly interpret and process your logs.
    - another example, when sending text, the server can specify that it wishes to send it as plain text using:
        - Content-Type: text/plain
    - When working with images, one would specify the image format, like this:
        - Content-Type: image/jpeg
    
    ```
    Request Example: 
    POST /api/images HTTP/1.1
    Host: nazu.com
    Content-Length: 102400
    Content-Type: image/jpeg
    
    image file meta-data here
    
    =================================
    Response Example: 
    HTTP/1.1 201 Created
    Server: Apache
    Connection: close
    Content-Length: 4096
    Date : Sun 05 Feb 2023         
    Content-type : application/json; charset=UTF-8
    ```