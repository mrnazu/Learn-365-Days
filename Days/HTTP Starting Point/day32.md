# HTTP

Starting point

# TCP/IP

- **TCP/IP** is a **Protocol** that stands for **Transmission Control Protocol/Internet Protocol**. It is a set of rules used by computers to **transmit data over the internet**. or for communication between host computers and clients or users with **packet switching.**

## Packet Switching

- **Packet switching** is a method of **actively sending data** in the form of packets over a network. Each packet contains **source** and **destination addresses**, as well as information about the **type** and **size** of the data.
    - **Source**  ⇒ The **sender** of data packets or **point of origin**, which is usually the computer or device that is sending out the data.
    - **Destination Address ⇒** TCP use for delivery of data between **two different end points.** The two end points are referred to as the **source** and **destination address**. that means destination address is the address to which it is **sent.**

## IP

- **IP** stands for **Internet Protocol** like i mentioned Earlier. It is the **language** or **ID** computers use to **communicate over the internet**. Think of IP and TCP like a game of baseball: IP is the diamond, TCP are the rules that everyone has to play by to be able to play on it! Without these rules, no one would know how to play baseball and have fun.

## Explain For Kid

> TCP/IP is like a **big highway with many roads.** All of the roads are **connected** but lead to **different places**. The job of TCP/IP is to guide your data just like a car through these roads so it gets to the correct destination. When you send an email, for instance, your computer talks to TCP/IP and tells it that the email needs to be sent. Then, TCP/IP looks at all of the roads or paths it knows about and figures out which one will get your email to its destination fastest. That way, your email arrives quickly!
> 

---

![tcp-main.png](HTTP%20a7d9e0ebad624df6943d9201fb5f8873/tcp-main.png)

---

## How HTTP work with TCP/IP (HTTP The Definitive Guide)

- [`https://www.mrnazu.com/index.html`](https://www.mrnazu.com/index.html)
- he browser extracts the host name
    - `mrnazu.com`
- The browser looks up the IP address for this hostname using **DNS**
    - 300.23.65.0
- The browser gets the **port** number
    - https ⇒ 443
    - http ⇒ 80
- The browser makes a **TCP** connection (After 3 Way Handshake)
    - IP: 300.23.65.0
    - Port: 443
- The browser sends an HTTP Request Message to the serve
- The browser reads the HTTP response message from the server
- The browser closes the connection

# HTTP

- **HTTP** stands for **Hypertext Transfer Protocol** and it used to transfer data on the internet. It works with TCP/IP using Transport layer. It works by establishing a connection between two hosts (client and server) over the TCP/IP protocols, in order for them to exchange requests and responses.
- The client sends an HTTP request message which contains the request method, URI, and HTTP version information, followed by a **MIME** type header and additional headers. The server then responds with a status line containing the HTTP version plus a success or failure code, followed by response headers. Finally, the response body is sent from the server to the client containing whatever data was requested. this all done by collaboration of HTTP and TCP/IP

# HTTPS

- **HTTPS** stands for **Hyper Text Transfer Protocol Secure** is an extension of the HTTP for secure communication. HTTPS allows for secured communication between clients and web servers through **encryption**, **authentication** and **data integrity**, making it difficult for hackers to **intercept (MITM)** or **modify** data sent between two endpoints. in short word **HTTPS** is a secure version of **HTTP.**
    - **Confidentiality** - It ensures that data remains confidential and prevents unauthorized access.
    - **Security** - It provides an additional layer of security by encrypting sensitive information (such as passwords or credit card numbers) before sending across the network.
    - **Authentication** - It helps to verify server identity, which can be used to protect against man-in-the-middle (mitm) attacks and other malicious activity.
    - **Compatibility** - It ensures compatibility between web browsers and other web-based applications using over 20 Secure Transport procedures like TLS/SSL (Secure Socket Layer).
    - **Reliability** - HTTPS requires certificate authority sign off from a trusted organization, ensuring greater reliability between the user and website connection compared to HTTP only connections
    - **Encryption** – All transmissions are encrypted which makes data more digitally secure than unencrypted transmissions

## How?

- HTTPS uses **Transport Layer Security** aka **TLS** to securely exchange data between the client and the server. TLS is a **cryptographic protocol** that provides secure communication. TLS establishes an **encrypted** connection between client and server by **authenticating** each communication session. HTTPS, when combined with the TLS protocol, creates an encrypted link between a web browser and a web server - ensuring all data sent between them remains private and secure.
- For example, when you use the website, your browser sends a lot of information including your usernames and passwords to other computers or web server. Without TLS, all this data could be sent in a plain text or seen and changed by someone listening in, like a hacker. TLS encrypt the data so that only the intended recipient can read it.
- **Secure Sockets Layer** aka **SSL** and **TLS** are both **cryptographic** **protocols** designed to provide **secure communication** and **data protection** over a **network**. The two protocols differ in their **compatibility**, **encryption strength** and overall **security**. SSL was the **first version** of the protocol and is an **older version of TLS** with **weaker encryption strength**. TLS is based on SSL but has been improved upon in **newer versions** and includes security features, such as Perfect Forward Secrecy, which make it more secure than SSL.
- To implement TLS on our website, we will need to purchase an SSL certificate from a trusted certificate provider and then install the certificate on our web server. Once the certificate is installed, we will need to configure our web server to use TLS/SSL protocol when serving pages.

---

![tls-proxy-diagram-removebg-preview-main.png](HTTP%20a7d9e0ebad624df6943d9201fb5f8873/tls-proxy-diagram-removebg-preview-main.png)

---

# Web Certificate

- A web certificate is a digital document used by website owners to verify their identity and encrypt the data. It is often used to secure online transactions. The certificate contains information about the website’s identity, including its name, address, contact details, public encryption key and other details. Web certificates are issued by trusted third parties aka Certificate Authorities (CA)

## Web symmetric key

- Symmetric Key is a **cryptographic** key used in web applications to **encode** and **decode** data. The symmetric key is shared amongst the two people involved in the communication (i.e. sender and receiver) and is kept secret from other parties.

### Website Public Key

- A **public key** is what others can use to send **encrypted** messages to you. It works in conjunction with your private key for encryption and decryption. A website public key a is a form of cryptography consisting of an encoded digital string which is created from a complex mathematical algorithm to identify the user. Through the use of the Website Public Key, communication between the server and any website can be authenticated. in short word it used for authenticated and secured communication

### Website Private Key

- It's the some as Public key but The private key must match its associated public key when transmitted from one entity to another to confirm identity and prove authenticity. that means private key does not posted publicly that only you have access to. Think of it like an ATM pin number: only you know it, and it allows you to spend your currency or access data. or if you have a website, anyone can use the public key posted on your site to initiate secure communication with you but can’t decrypt any information sent using the public key without also having access to your private key

---

![symmetric-vs-asymmetric-symmetric-example-removebg-preview-main.png](HTTP%20a7d9e0ebad624df6943d9201fb5f8873/symmetric-vs-asymmetric-symmetric-example-removebg-preview-main.png)

---

## Decrypts Symmetric key with its Private key

- The public key is used to encrypt data, while the private key can be used both to decrypt the same data.
- To use the asymmetric cipher to decrypt a symmetric key with its private key, you'll need to start by generating an RSA or ECC public-private key pair. Once you have your keys, you'll then encrypt your symmetric session/transport keys using each user's public RSA/ECC key. Those encrypted keys can then only be decrypted with that user's corresponding private RSA/ECC key.
- For Example, let's say Nazu wants to securely transmit confidential information over a network connection to Nazi. To do that, Nazu will first generate an RSA or ECC public-private key pair for himself, and Nazi would do the same for himself. Nazu then uses Nazi’s public RSA/ECC Key to encrypt his symmetric transport session/key before sending it to him in encrypted form over their unsecured communication channel. Finally, Nazi will use his own corresponding Private RSA/ECC Key to decrypt the symmetrically-encrypted session/transport keys sent by Nazu, thus enabling secure communication between both parties.

---

![pgp-removebg-preview-main.png](HTTP%20a7d9e0ebad624df6943d9201fb5f8873/pgp-removebg-preview-main.png)