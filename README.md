# NetAuto

NetAuto is a basic network reconnaissance tools that automates enumeration of services, protocols and ports, ideal for penetration testing environments and network scanning.

This tool performs port scans and service detection to perform further enumeration scans using different third-party tools.

It performs **no automated exploitation**.

# Origin
It was inspired by the following ethicaL hacking notes that provide numerous opportunities of scanning multiple targets in the form of IP addresses

# Installation
Requirements of utilizing this tool must be met by installing the latest available packages
```
sudo apt-get update
```

Additionally, it requires the usage of Python, Python 2, Python 3 and pip, which can be installed on Kali Linux by performing the following commands:
```
sudo apt-get install python
sudo apt-get install python2
sudo apt-get install python3
sudo apt-get install python3-pip
sudo apt-get install pip
sudo apt-get install pipx
```

If you want to ensure that all of these packages are installed, perform those following commands instead:
```
sudo apt-get install python python2 python3 python3-pip pip pipx
```

These following tools need to be installed and put in /opt directory in order to utilize the following script:
```

nmap
onesixtyone
snmpwalk
snmpcheck
openssl
ssh-audit
ssh-keyscan
dif
finger
ntpq
impacket-rpcdump
/usr/share/doc/python3-impacket/examples/rpcdump.py
/usr/share/doc/python3-impacket/examples/rpcmap.py
/opt/tools/MSRPC/IOXIDResolver.py
nmblookup
nbtscan
enum4linux
rpcclient
netexec
smbmap
crackmapexec
impacket-looksupid
ldapsearch
ike-scan
curl
rsync
python2 /opt/tools/IPP/PRET/pret.py
rusers
rpcinfo
python /opt/tools/Squid/spose/spose.py
svn
sudo python3 /opt/tools/CISCO_Smart_Install/SIETpy3/siet.py
opalopc
python /opt/tools/Docker_Registry/DockerRegistryGrabber/drg.py
GlusterFS/gluster
nikto
whatweb
webtech
webanalyze
apiti
wafw00f
/opt/tools/HTTP/WhatWaf/whatwaf
cmsmap
wpscan
joomscan
python3 /opt/tools/HTTP/CMSeek/cmseek.py
redis-cli
oscanner
tnscmd10g
odat sidguesser
odat-libc2.12-x86_64 passwordguesser -s $IP -d XE --accounts-file accounts/default.txt 
```

Perform those following commands if you want to install simultaneously:
```
sudo apt-get install python python2 python3 python3-pip pip pipx
```

You can utilize the bash script by donwloading the git clone by the following:
```
git clone https://github.com/eliaz5536/netauto.git
```

Make sure you provide the linux permission to execute the file before launching the bash script:
```
chmod +x netauto
```

Launch NetAuto bash script file:
```shell
./netauto -i <TARGET_IP_ADDRESS>
```
It will generate reports from NMAP that will display all ports that are running under the following target.

Once it is generated, view the following ports and list all the ports that are reported for you to scan,
by performing this following command:
```
./netauto -i <TARGET_IP_ADDRESS> -p <TARGET_PORTS>
```

# Usage 
```

            ███╗   ██╗███████╗████████╗██╗    ██╗ ██████╗ ██████╗ ██╗  ██╗              
            ████╗  ██║██╔════╝╚══██╔══╝██║    ██║██╔═══██╗██╔══██╗██║ ██╔╝              
            ██╔██╗ ██║█████╗     ██║   ██║ █╗ ██║██║   ██║██████╔╝█████╔╝               
            ██║╚██╗██║██╔══╝     ██║   ██║███╗██║██║   ██║██╔══██╗██╔═██╗               
            ██║ ╚████║███████╗   ██║   ╚███╔███╔╝╚██████╔╝██║  ██║██║  ██╗              
            ╚═╝  ╚═══╝╚══════╝   ╚═╝    ╚══╝╚══╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝              
███████╗███╗   ██╗██╗   ██╗███╗   ███╗███████╗██████╗  █████╗ ████████╗ ██████╗ ██████╗ 
██╔════╝████╗  ██║██║   ██║████╗ ████║██╔════╝██╔══██╗██╔══██╗╚══██╔══╝██╔═══██╗██╔══██╗
█████╗  ██╔██╗ ██║██║   ██║██╔████╔██║█████╗  ██████╔╝███████║   ██║   ██║   ██║██████╔╝
██╔══╝  ██║╚██╗██║██║   ██║██║╚██╔╝██║██╔══╝  ██╔══██╗██╔══██║   ██║   ██║   ██║██╔══██╗
███████╗██║ ╚████║╚██████╔╝██║ ╚═╝ ██║███████╗██║  ██║██║  ██║   ██║   ╚██████╔╝██║  ██║
╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝    ╚═════╝ ╚═╝  ╚═╝


Network Enumeration Automator with Nmap, Rustscan & Masscan
Usage: Netauto -i <ip_address> [options]
 
Arguments
  ip_address              Target internet protocol address of the identified device
 
Options:
  -i                      Scan IP address of the target device
  -p                      Scan ports of the targets device
 
Timing options:
  -T0                     Paranoid
  -T1                     Sneaky
  -T2                     Polite
  -T3                     Normal (Default)
  -T4                     Aggressive
  -T5                     Insane

```

```

            ███╗   ██╗███████╗████████╗██╗    ██╗ ██████╗ ██████╗ ██╗  ██╗              
            ████╗  ██║██╔════╝╚══██╔══╝██║    ██║██╔═══██╗██╔══██╗██║ ██╔╝              
            ██╔██╗ ██║█████╗     ██║   ██║ █╗ ██║██║   ██║██████╔╝█████╔╝               
            ██║╚██╗██║██╔══╝     ██║   ██║███╗██║██║   ██║██╔══██╗██╔═██╗               
            ██║ ╚████║███████╗   ██║   ╚███╔███╔╝╚██████╔╝██║  ██║██║  ██╗              
            ╚═╝  ╚═══╝╚══════╝   ╚═╝    ╚══╝╚══╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝              
███████╗███╗   ██╗██╗   ██╗███╗   ███╗███████╗██████╗  █████╗ ████████╗ ██████╗ ██████╗ 
██╔════╝████╗  ██║██║   ██║████╗ ████║██╔════╝██╔══██╗██╔══██╗╚══██╔══╝██╔═══██╗██╔══██╗
█████╗  ██╔██╗ ██║██║   ██║██╔████╔██║█████╗  ██████╔╝███████║   ██║   ██║   ██║██████╔╝
██╔══╝  ██║╚██╗██║██║   ██║██║╚██╔╝██║██╔══╝  ██╔══██╗██╔══██║   ██║   ██║   ██║██╔══██╗
███████╗██║ ╚████║╚██████╔╝██║ ╚═╝ ██║███████╗██║  ██║██║  ██║   ██║   ╚██████╔╝██║  ██║
╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝    ╚═════╝ ╚═╝  ╚═╝


IP: 192.168.69.10
PORT(S): 
1) Network Scan
2) Scan Unknown Ports
3) UDP/TCP Scan
4) Quit
Select an option in Nmap (enter the number): 

```

```
Select an option in Nmap (enter the number): 1
Default 
1) default
2) -T1
3) -T2
4) -T3
5) -T4
6) -T5
7) Quit
Please enter the min-rate of your choice: 

```

# Results
The following results of these scans will produce NMAP directory and the rest of enumeration programs for each of the following ports through its name that will store and output all enumeration results of specified protocols through either -oN flag from NMAP or use tee to output the results into specified location 
```
Netauto
└── 192.168.69.10
    └── DEFAULT
        ├── TCP_scan.txt
        ├── aggressive_scan.txt
        ├── port_scans.txt
        ├── script_scan.txt
        ├── stealth_scan.txt
        └── vulnerability_scan.txt

```

