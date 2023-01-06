# **Finding Bugs With Nuclei**

**Nuclei** v0.9 is a vulnerability scanner to identify vulnerabilities and security issues in **web** applications. It is an **open source** tool that automates the process of identifying valid attack vectors via powerful templates and configuration files. Nuclei’s main feature is its ability to quickly scan large parts of the web application landscape based on input sources such as IP address, domain name, CIDR ranges, etc. Nuclei can detect common vulnerabilities as well out-of-the-box as well make it easy for users to create custom vulnerability scans. The tool is primarily programmed in the Go programming language, with part of the code written in Rust as well. Nuclei offer to scan for various protocols, including **DNS**, **HTTP**, **TCP**, and **APIs**. 

# Installation of Nuclei

- Firstly we need to clone the Nuclei repository from the GitHub page:
    
    ```bash
    ┌──(nazu㉿Nazu)-[~]
    └─$ git clone https://github.com/projectdiscovery/nuclei
    ┌──(nazu㉿Nazu)-[~]
    └─$ cd nuclei
    ```
    
- Now we’ll build the binaries as well as install dependencies by running go build:
    
    ```bash
    ┌──(nazu㉿Nazu)-[~]
    └─$ make all && make deps
    ```
    
- The last step is to execute nuclei binary using:
    
    ```bash
    ┌──(nazu㉿Nazu)-[~]
    └─$ ./nuclei -h
    ```
    
- List all available templates
    
    ```bash
    ┌──(nazu㉿Nazu)-[~]
    └─$ nuclei -tl
    ```
    
    ```bash
    #easy mode
    ┌──(nazu㉿Nazu)-[~]
    └─$ nuclei -u https://example.com/
    
    #list of target
    ┌──(nazu㉿Nazu)-[~]
    └─$ nuclei -l target_list.txt
    
    ```
    

[Ultimate nuclei Guide](https://blog.projectdiscovery.io/ultimate-nuclei-guide/)
