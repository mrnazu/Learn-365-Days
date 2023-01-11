# **API Reconnaissance aka Recon**

API Reconnaissance is the process of gathering information from public Application Programming Interface (API) endpoints and using it to build an understanding of what data is exposed, the format of the responses, and who can access them. It involves leveraging open APIs to understand how the target systems are structured, what assets are present, and what their security posture looks like.

### **Here is an example of how to perform API reconnaissance:**

**.**
1. Start by gathering public information - Use search engines and open sources such as domain registrar websites and public code repositories (e.g GitHub) to gather publicly available information about the target organization’s APIs. Try searching for terms like “`**API**`”, “`**REST**`”, “`**Web Service**`”, or the organization name itself.

2. Check for **Documentation** - Many APIs provide user manuals on their websites that outline **`endpoints`**, `**parameters**`, and other details related to using the API. Make sure you read all relevant documentation first before performing any testing.

3. Intercept Requests & Responses  - Use a proxy tool like **`Burp Suite`** or **`ZAP Proxy`** to intercept HTTP requests and responses between your browser and the target organization's **server/application**. This will help you understand what data is being exchanged between your application and the `server/application`.

4. Test Parameter Enumeration - Test parameter enumeration by trying to invoke an endpoint with different request parameters than those specified in the documentation (if available). This can help you identify hidden endpoints which may not have been documented anywhere else but are still accessible through the API interface.

### EX-2 || Resource ⇒ API Sec University

Another way to find an API provided by a target is to look around the target's landing page. Look through a landing page for links to API or development portal. When searching for APIs there are several signs that will indicate that you have discovered the existence of a web API. Be on the lookout for obvious URL naming schemes:

- [`https://example.com/api/v1`](https://target-name.com/api/v1)
- `https://example.com/v1`
- `https://example.com/doc`
- `https://dev.example.com/rest`

**Look for API indicators within directory names like:**

`/api, /api/v1, /v1, /v2, /v3, /rest, /swagger, /swagger.json, /doc, /docs, /graphql, /graphiql, /altair, /playground`

**Also, subdomains can also be indicators of web APIs:**

**`api**.example.com`

**`uat**.example.com`

**`dev**.example.com`

**`developer**.example.com`

**`test**.example.com`

**HTTP Responses that include statements like:** **`{"message": "Missing Authorization token"}`

**Third-Party Sources:**

**Gitub:** [`https://github.com/`](https://github.com/)

**Postman Explore:** [`https://www.postman.com/explore/apis`](https://www.postman.com/explore/apis)

**ProgrammableWeb API Directory:** [`https://www.programmableweb.com/apis/directory`](https://www.programmableweb.com/apis/directory)

**APIs Guru:** [`https://apis.guru/`](https://apis.guru/)

**Public APIs Github Project:** [`https://github.com/public-apis/public-apis`](https://github.com/public-apis/public-apis)

**RapidAPI Hub**: [`https://rapidapi.com/search/`](https://rapidapi.com/search/)

# ****Passive Reconnaissance****

     Example of Google Dorking ⇒ `title:”api” site:”example.com”`

Example of Git Dorking ⇒ `search for your target API` , `extension:json target`

### **TruffleHog**

Tool for automatically discovering exposed secrets. ⇒ `$ sudo docker run -it -v "$PWD:/pwd" trufflesecurity/trufflehog:latest github --org=exampleTarget`

### ****`API Directories, Shodan and Wayback Machine`****

# **Active Reconnaissan - like web recon**

### `nmap, amass, gobuster, ****Kiterunner, DevTools, postman and so on****`

`nmap -sV --script=http-enum <target> -p 80,443,8000,8080`

`amass enum -active -d target-name.com | grep api`

******Kiterunner ⇒ best tool for discovering API endpoints and resources.******

`kr scan [HTTP://](http://127.0.0.1/)target -w api_wordlist`
