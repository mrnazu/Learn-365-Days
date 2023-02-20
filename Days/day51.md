# Sessions & Cookies

# What is Session

- Session in web app is a way to store information about a user's interaction with a website. It allows the website to remember the user's preferences and settings over multiple visits.
- For example, when you log into an online banking website, the website will create a session for you. This session will store your login information and other preferences such as language, currency, etc. When you navigate to different pages on the website, the session will be used to keep track of your activity and provide personalized content.

---

# What is Cookie

- A cookie is a small piece of data that is stored on a user's computer when they visit a website. It is used to remember information about the user, such as their preferences or login details.
- For example, when you log into a website, the website may store your username in a cookie so that you don't have to enter it every time you visit the site.

---

## How Session and Cookies Work Together

- For example, when a user visits a website, the server creates a unique session ID and stores it in a cookie on the user's computer. When the user visits other pages on the website, the server can read the session ID from the cookie and use it to identify which user is making the request. This allows the server to keep track of what pages the user has visited, what items they have added to their shopping cart, and any other information that needs to be remembered across multiple page requests.
- The session ID is also used to ensure that only authorized users can access certain parts of the website.
    - For example, if a user logs into their account, they will be given an authentication token that is stored in their session cookie. This token is then used by the server to verify that they are logged in when they make requests for restricted content.

---

## How Sessions Work

- A web app session is a period of time in which a user interacts with a web application. During this period, the user's activity is tracked and stored in the server's memory.
- For example, when a user logs into an online banking application, they are assigned a unique session ID. This ID is used to track their activity within the application. Every time the user performs an action, such as transferring money or checking their balance, this information is stored in the server's memory. When the user logs out or closes their browser window, the session ends and all of their data is deleted from the server's memory.

---

## How Cookies work

- For example, when you log into a website, the website will store a cookie on your computer so that it can remember who you are when you come back later. When you return to the website, it will read the cookie and recognize you as the same user. This allows you to stay logged in without having to enter your credentials every time.
- Cookies can also be used to store preferences such as language settings or font size. This allows the website to remember your preferences and display them accordingly when you return.

---

# Differences between them

- Cookies
    - A web cookie is a small piece of data stored on the user's computer by the web browser.
    - Cookies are used to store information about the user such as their preferences, login information, and other data.
    - Cookies are sent back to the server with each request, allowing the server to identify the user and customize their experience.
    - Cookies are stored on the user's computer and can be accessed by any website that has set a cookie for that domain.
- Sessions
    - A session is a server-side storage mechanism that stores data specific to a particular user session.
    - Unlike cookies, sessions are not stored on the user's computer but instead on the server.
    - Sessions allow for more secure storage of data since they are not accessible by any website other than the one that created them.
    - Sessions also allow for more complex data structures to be stored since they can store objects as well as simple strings or numbers.

---

# Advantages of Session and Cookies

- Advantages of Sessions
    - Sessions are more secure than cookies as they are stored on the server side and not visible to the user.
    - Sessions can store more data than cookies as they are not limited by size restrictions.
    - Sessions can be used to store sensitive information such as passwords, credit card numbers, etc., which should not be stored in a cookie.
- Advantages of Cookies
    - Cookies are easier to implement than sessions as they do not require any server-side code or database setup.
    - Cookies can store small amounts of data which is useful for tracking user preferences or other small pieces of information that need to be remembered between visits to a website.
    - Cookies can also be used for authentication purposes, allowing users to stay logged in without having to re-enter their credentials each time they visit the website.

---

## How session and cookies can be vulnerable

- Session and cookies can be vulnerable to a variety of attacks, including session hijacking, cross-site scripting (XSS), and cross-site request forgery (CSRF).

---