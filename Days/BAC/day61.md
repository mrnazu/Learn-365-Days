# BAC

# Broken Access Control

![BAC.png](BAC%2020cc96eb33b94b62bd97a6cfdc3c637d/BAC.png)

Broken Access Control occurs when incorrect authorization checks are implemented incorrectly, allowing unauthorized users to gain access to privileged resources or functions.

An example of Broken Access Control is a website that provides user accounts and allows users to control their own accounts. If the site owner had not applied sufficient restrictions, it would be possible for an attacker to gain access to someone else's account by entering their username. The attacker could then make changes to the account, view private information, and potentially perform other malicious activities.

---

In the first picture i represented **vertical** BAC since i am execute functionality that can not be executed by any user of my access level. I'd need a user of a higher privilege level than mine to be able to execute this functionality under normal operations.

When we talk about **horizontal** BAC defects we are talking about functionality that we would normally be able to execute but simply not on that specific object. we know this as an IDOR (Insecure direct object reference)

![ideo.png](BAC%2020cc96eb33b94b62bd97a6cfdc3c637d/ideo.png)

# Some Term

## Authentication:

- The process or action of proving or showing something to be true, genuine, or valid.

![Authentication_vs_Authorization.png](BAC%2020cc96eb33b94b62bd97a6cfdc3c637d/Authentication_vs_Authorization.png)

## Session Management:

- The process of securely handling multiple requests to a web-based application or service from a single user or entity.

![session.png](BAC%2020cc96eb33b94b62bd97a6cfdc3c637d/session.png)

## Access Control:

- Determines Whether the user is allowed to carry out the action that they are attempting to perform.
    - once you have authenticated to the application and got in your session token you want to perform certain actions. so the application needs to determine if you are allowed to carry out that action.
        - For example, an organization might have a policy that only administrators are allowed to access and modify company information while all other users have read-only access. A web application access control system would ensure that only the designated administrators were able to make changes while other users were restricted from any specified actions.

---

---

---