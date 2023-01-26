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
        
        ![source code](https://user-images.githubusercontent.com/108541991/214885004-6b004f59-dd8e-4ee0-acef-96665dcfb7f5.jpg)
    
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
    
    ![portal](https://user-images.githubusercontent.com/108541991/214885173-a3768137-57a6-4720-955b-77fe2815ea29.jpg)

    
    **blog.futurevera.thm:**
    
    ![blog](https://user-images.githubusercontent.com/108541991/214885264-65984691-8458-44f4-ad1d-b9ad80fd7ffc.jpg)

    
    **support.futurevera.thm: seems intersting🙂😃**
    
    ![support](https://user-images.githubusercontent.com/108541991/214885387-20925164-55d4-4d9a-aa46-7eb3e7b3f4a0.jpg)

  
    **we found another domain on the certficate | add to /etc/hosts then boom💣💣**
    ![dom-dom](https://user-images.githubusercontent.com/108541991/214885493-0c21f8ed-ca3b-4dde-bafd-8d900bd2f2b7.jpg)

    
    

# Flag ⇒ `flag{beea0d6edfcee06a59b83fb50ae81b2f}`

---

## Improved skills

- nothing but checking certificate is importnant😕

## Used tools

- rustscan
- dev tool
- knockpy

# **The End**
