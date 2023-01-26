# TakeOver

Category: Web
Difficulty: Easy
Platform: TryHackMe
Status: In progress
Tags: TakeOver, subdomain

***TABLE OF CONTENTS:***

- **[Intro](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)**
    - [help us](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)
- [Recon & Hacking](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)
- [Flag](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)
- [Improved skills](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)
- [Used tools](https://www.notion.so/TakeOver-e6a7eafa779f414698ef9e8e047b68b1)

---

# Intro

- I am the CEO and one of the co-founders of futurevera.thm. In Futurevera, we believe that the future is in space. **We do a lot of space research and write blogs about it**. We used to help students with space questions, but we are rebuilding our support.

---

- **Recon & hacking**
    
    **First of all:**
    
    `sudo nano /etc/hosts` then add this `10.10.6.84 futurevera.thm`
    
    **We know what we do that means our task is all about sub domain enumration. seems easy😊**
    
    - **SSH is open🥸**
    1. **btw, we can check the source code if there is a mentioned sub-domain**
        
        **but there is nothing intersting thing😢**
        
        ![source code.jpg](TakeOver%20e6a7eafa779f414698ef9e8e047b68b1/source_code.jpg)
        
    
    **Let's go ahead and enumerate a subdomain using knockpy(my fav sub-domain scanner tools ever!)** 
    
    ```
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/TakeOver]
    └─$ knockpy futurevera.thm
    # then we found: 
    portal.futurevera.thm 
    blog.futurevera.thm
    support.futurevera.thm
    ```
    
    **So now, we have to add this portal subdomain into `/etc/hosts`**
    
    - **3 thing you have to do while testing subdomain takeover.**
        - **the first one is checking source code like before,**
        - **the seconde one is checking domina under a domain maybe 3 or 4 times dom1.dom2.dom3.dom4.maindom…. using tools such as knockpy, amass..**
        - **the third one is osint and checking certificate**
    
    **portal.futurevera.thm:**
    
    ![portal.jpg](Resources/TakeOver%20e6a7eafa779f414698ef9e8e047b68b1/portal.jpg)
    
    **blog.futurevera.thm:**
    
    ![blog.jpg](Resources/TakeOver%20e6a7eafa779f414698ef9e8e047b68b1/blog.jpg)
    
    **support.futurevera.thm: seems intersting🙂😃**
    
    ![screen shot](Resources/TakeOver%20e6a7eafa779f414698ef9e8e047b68b1/support.jpg)
    
    screen shot
    
    **we found another domain on the certficate | add to /etc/hosts then boom💣💣**
    
    ![dom-dom.jpg](Resources/sTakeOver%20e6a7eafa779f414698ef9e8e047b68b1/dom-dom.jpg)
    

# Flag ⇒ `flag{beea0d6edfcee06a59b83fb50ae81b2f}`

---

## Improved skills

- nothing but checking certificate is importnant😕

## Used tools

- rustscan
- dev tool
- knockpy

# **The End**
