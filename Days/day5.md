# Insecure Deserialization

- Serialization
    - Serialization is the process of converting or turning an object into a format that can be restored.
- Deserialization
    - Deserialization is a process of converting or turning serialized data or in other word it's the reverse of Serialization. then it will convert data back into its original state in a web app.
- For Example
    - A user may have **username** and **password** as two data. `username = nazu & password = nazu1234`This application may need to save these details somewhere, so that in the future, the user **nazu** can login and get **authenticated**. This might be done by saving these details in a **local file**, **database** or even some **remote** **database** over the network. In that case, the object must be **converted** or **encoded** into a **format** that can be **easily transmitted** or **saved**. This is known as **Serialization**. When the application needs to fetch the object back, it just performs the reverse operation. which is known as **Deserialization.**
- Example 2
    - Serialization
        - We convert this object into a format that can be easily stored or transmitted. For example, let's say that our example Person's details are as follows:
            
            `Name = nazu
            Age = 100
            Gender = Male`
            
        - We could serialize this information by converting it into a JSON string as follows `{"name":"nazu","age":100,"gender":"Male"}` This makes it easy to store and transmit our data with minimal overhead.
    - Deserialization
        - Deserialization is the inverse of serialization - converting structured data such as JSON back into an object.
            
            `Name = nazu
            Age = 100
            Gender = Male`
            
- Example 3
    - PHP forum uses **PHP Object Serialization** to save a “**Super”** cookie, containing the user’s user ID, role, password hash, and other states:
        
        **Regular User Cookie:**
        
        - `a:4:{i:0;i:132;i:1;s:7:”nazu”;i:2;s:4:”user”;
        i:3;s:32:”b6a8b3bea87fe0e05022f8f3c88bc960";}`
        
        An **attacker** changes the **Serialized** object to give themselves **admin** Privileges:
        
        **Admin’s Super Cookie:**
        
        - `a:4:{i:0;i:1;i:1;s:5:”attacker”;i:2;s:5:”admin”;
        i:3;s:32:”b6a8b3bea87fe0e05022f8f3c88bc960";}`

# Methodology to Find Insecure De-serialization Vulnerabilities

- First, Analyze the source code to find the parts of the application where objects are deserialized.
- When an object is deserialized, look for potential attack vectors such as user-supplied data, and then evaluate if it goes through security checks before being deserialized
- It’s also essential to check API endpoints that accept serialized objects as parameters and handle resource access control logic in order to verify they’re securely configured.
- Set-up automate scanning tool like burp suite and then utilize fuzzing techniques, including sending invalid and unexpected payloads in order to discover how the application reacts by looking at responses generated from queries provided with malicious data
- Manual testing such as modifying requests using specific exploit formats like YAML or JSON files sent via POST methods in order to identify further insecure deserialization issues

[Insecure deserialization Lab](https://portswigger.net/web-security/all-labs#insecure-deserialization)
