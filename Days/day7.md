# **Open Redirect**

An open redirect is an endpoint on a vulnerable website, or Open redirect are when a web page takes an invalidated user-submitted parameter and uses it to redirect the user to another URL or Domain. Generally, this URL is submitted via **GET** or **POST** requests from the browser address bar or as a part of a form submission.

# Types of Open Redirect

- Parameter Based or Vulnerable Parameters
    - This type of open redirect vulnerability occurs when user input is **allowed to control a parameter** within the URL and can be used to point the user toward an evil domain or something. For example, if a website allows GET parameters such as “turn” `?turn=` within the URL, then an attacker could craft a URL using this parameter and point it to any destination they would like, for instance [`http://example.com?turn=http://evil.com](http://example.com/?returnto=http://maliciousurl.com).`
- Misconfigured Redirects or Server Misconflagration
    - Misconfigured redirects occur when the server allows requests that contain untrusted input in URLs when an application is trying to perform a redirection. For example, if a website is configured so that any request with `/redirect` will try and move you elsewhere, then hackers could target this by crafting malicious URLs such as [`http://example.com/redirect?url=http://evil.com`](http://example.com/redirect?url=http://maliciousurl.com)
- Referer-Based Redirects - HTTP Header
    - This type of Redirection occurs when the web application uses the HTTP **Referer** header as part of its redirection logic. This allows hackers to trick website users to evil or elsewhere locations by injecting a malicious URL into the HTTP referer header.
    - Example: Let’s say an attacker wants to use an open redirect vulnerability on [`https://victim.com`](https://victim.com/). then [`http://victim.com/?redirect=http%3A%2F%2Fevil.com%2Fmalicious`](http://victim.com/?redirect=http%3A%2F%2Fevil.com%2Fmalicious) If [`victim.com`](http://victim.com/) is vulnerable to `referer-based redirects`, then visiting the malicious link will cause [`victim.com](http://victim.com/)’s` server to read the HTTP referer field and automatically perform a redirection to [`http://evil.com/malicious`](http://example.com/malicious)
    - There are many different types of redirects
        - Header Based Redirects
            
            `Location: [https://www.evil.com/](https://www.evil.com/)`
            
        - Meta tag
            
            `<meta http-equiv = "refresh" content = "0;url=https://www.evil.com/" />`
            
        - DOM-Based Redirects
            
            `window.location = '[https://www.evil.com](https://www.attacker.com/)'`
            
            and so on…….
            
    
    # T**rick to find Open Redirection**
    
    - Test URL parameters - manually check GET query strings and POST request bodies for parameters.
    - Pay attention to third-party components - web applications often use third-party components such as APIs and social media widgets that may have their own configuration settings and controls that may be vulnerable to redirect.
    - Simple Trick (Credit: [febinrev](https://twitter.com/febinrev) )
        - If the Applictaion have a user Sign-In/Sign-Up feature, then register a user and log in as the user.
        - Go to your user profile page , for example: [`samplesite.me/accounts/profile`](http://samplesite.me/accounts/profile)
        - Copy the profile page's URL
        - Logout and Clear all the cookies and go to the homepage of the site.
        - Paste the Copied Profile URL on the address bar
        - If the site prompts for a login , check the address bar , you may find the login page with a redirect parameter like the following
            
            [`https://samplesite.me/login?next=accounts/profile`](https://samplesite.me/login?next=accounts/profile)
            
            [`https://samplesite.me/login?retUrl=accounts/profile`](https://samplesite.me/login?retUrl=accounts/profile)
            
        - Try to exploit the parameter by adding an external domain and load the crafted URL
        eg:- [`https://samplesite.me/login?next=https://evil.com/`](https://samplesite.me/login?next=https://evil.com/) or [`https://samplesite.me/login?next=https://samplesite.me@evil.com/](https://samplesite.me/login?next=https://samplesite.me@evil.com/)` (to beat the bad regex filter)
        - If it redirects to [evil.com](http://evil.com/) , thers's your open redirection bug.
    
    # **Open Redirection Bypass**
    
    To bypass open redirection it is important for developers to be aware of how their applications use user expected URLs and then take precautions/ቅድመ ጥንቃቄዎች like whitelisting allowed redirects that are accepted by their application or etc.. 
    
    Example: [`http://www.example.com/redirect?url=www.example.com](http://www.example.com/redirect?url=www.example.com),` while malicious users could modify it adding other URLs at the end with the intent of redirecting users in unexpected places e.g [`www.examplesite.com/redirect?url=http://evil.com/`](http://www.examplesite.com/redirect?url=http://evil.com/). Therefore developers should check requests coming in and filter out non-whitelisted URLs before allowing any further redirects in order to avoid any kind of malicious activities like open redirection bypass attacks with cleverly crafted requests containing malicious URLs! maybe **regex.**
    
    ### Mind Tricks for Hackers:
    
    - Think outside the box for complex problems – developers unusual yet effective tactics such as lateral thinking (thinking outside the confines of familiar patterns) which could lead you down an unexpected path to success with security loopholes & system vulnerabilities.
    - Research more and more and Keep up with advances in technology – Remain well informed about changes & any new developments when it comes to hardware/software technologies related to hacking by subscribing to newsletters & actively participating in online discussions on cyber topics frequently!
