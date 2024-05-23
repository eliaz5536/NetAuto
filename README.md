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
git clone <INSERT URL HERE>
```


# Usage 
```
SHOW USAGE HERE
```

# Results
The following results of these scans will produce NMAP directory and the rest of enumeration programs for each of the following ports through its name that will store and output all enumeration results of specified protocols through either -oN flag from NMAP or use tee to output the results into specified location 
```
show file location here and directory of how it is performed
```

