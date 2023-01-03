# What is Pen-test?
- Pen-Testing is a Collection of Action with a Specifc Goal. and it have 5 diffrent phases. The whole goal of a pen test is so much more than just finding issues or finding vulnerabilities and exploiting it, The first things is You have to guide your client in first determining a goal that is Smart: **Specific**, **Measurable**, **Attainable**, **Relevant**, and **Timely**.
- Atleast give us a solid basis on which we can lean to determine our strategy.


# In scope/Out of scope

- Whatever methodology you pick, you will always be bound to a certain scope. If you are unsure about anything regarding the scope or anything else, you have to ask the client about yout scope and out of scope.
- Don’t start randomly attacking websites or something.. make sure your tools are also set to properly take this scope in mind.

# Being Ethical

- You do have to put your client first generally speaking though. You have to protect them from unethical actors and from company espionage. You will have signed an NDA by now with your client.

# Types of a Pen-test

- Network pentest
    - Network-related pen tests are often relying heavily on tools. You want to enumerate as much as possible and it usually starts with a port scan. The goal is often to exploit **logic vuln**, **exploit misconfigurations** or **weaknesses** in the architecture or deny access to the infrastructure through a **DoS** attack.
- Website pentest
    - It's the some as network pen-testing but The goal is to get a reverseshell to get on the server, find a web exploit such as XSS, CSRF and etc, get access to files on thesystem or deny access to the infrastructure with a DoS attack.
- API pentest
    - This type is marked by the usage of tools such as **postman** and **ReadyAPI**. We can also write our own code in **python** for example for interaction with an **API**. It has its own **top 10 vulnerability types drafted by OWASP** and there is **no set methodology** for this. It often relies heavily on **documentation**, **technical knowledge** of the tester, and discovery of attack surface. We want to try and exploit **logic**, find **weaknesses** and **unexplored attack surfaces**, or deny access through a **DoS** attack
- Organization pentest
- IOT pentest
- Cloud-hybrid infrastructure testing
- Web 3.0 pentest
- Physical pentest
- Automotive pentest
- Social engineering
- Metaverse pentest

# Deliverables of a Pentest

- When we perform a pentest, we need to have proof of our work or PoC and we need to be able to brief our clients in a way they can understand through documentation. (like bug report)
    - NDA (Non-Disclosure Agreement)
    - Test Plan
    - Test Report
        - Vulnerabilities found
        - Steps to reproduce
        - Actual result
        - Expected result
        - Summary
        - CVSS score
    - Debriefing
