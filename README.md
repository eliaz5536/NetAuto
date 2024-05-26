![automated_network_enumerator](https://github.com/eliaz5536/NetAuto/assets/5835036/55eafde0-f387-49fa-913a-bb4436bb797e)

# Demos


# NetAuto
NetAuto is a basic network reconnaissance tools that automates enumeration of services, protocols and ports, ideal for penetration testing environments and network scanning.

This tool performs port scans and service detection to perform further enumeration scans using different third-party tools.

It performs **no automated exploitation**.

# Origin
It was inspired by the following ethicaL hacking notes that provide numerous opportunities of scanning multiple targets in the form of IP addresses

# Requirements
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

The following tools that are utilized for pure port scanning and service discovery requires installation
These following tools need to be installed and put in /opt directory in order to utilize the following script:
| Nmap         | OpenSSL    | Netcat             | onesixtyone | snmpwalk              | snmp-check    | dif       |
|--------------|------------|--------------------|-------------|-----------------------|---------------|-----------|
| finger       | ntpq       | impacket-rpcdump   | rpcdump     | rpcmap                | IOXIDResolver | nmblookup |
| nbtscan      | enum4linux | rpcclient          | enum4linux  | enum4linux-ng         | netexec       | smbmap    |
| crackmapexec | smbclient  | impacket-looksupid | IKE-Scan    | PRET                  | rsync         | rpcinfo   |
| spose        | svn        | SIETpy3            | OpalOPC     | DockerRegistryGrabber | Nikto         | WhatWeb   |
| WebTech      | WebAnalyze | Wapiti             | wafw00f     | WhatWaf               | CMSMap        | WPScan    |
| JoomScan     | CMSeeK     |                    |             |                       |               |           |



You can install most of the packages through apt package by doing the following 
```
sudo apt-get install nmap snmpwalk snmpcheck openssl ssh-audit ssh-keyscan dif finger ntpq impacket-rdcdump nmblookup nbtscan enum4linux rpcclient netexec smbmap crackmapexec impacket-looksupid ldapsearch ike-scan curl rsync rusers rpcinfo svn opalopc nikto whatweb webtech webanalyze apiti wafw00f cmsmap wpscan redis-cli oscanner tnscmd10g  
```

Several third-party require cloning repositories to be cloned into a specified directory 
```
git clone <repositories over here>
```


Perform those following commands if you want to install simultaneously:
```
sudo apt-get install python python2 python3 python3-pip pip pipx
```

# Installation
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

## Symlink Integration
You can add symlink to call the following program without using 
```

```

# Usage 
It is recommended that you run sudo on this script since it requires specific permissions to execute Nmap commands.

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


Network Enumeration Automator with Nmap
Usage: Netauto -i <ip_address> [options]
Options:
  -h, --help                      Help & Usage
  -i, --ip                                Scan IP address of the target device
  -p, --ports                     Scan ports of the targets device
  -t, --timing                    Set NMAP timing minrate option
 
Timing minrate options:
  -T0                     Paranoid
  -T1                     Sneaky
  -T2                     Polite
  -T3                     Normal (Default)
  -T4                     Aggressive
  -T5                     Insane
 
Perform reconnaissance: 
netauto -i 192.168.69.10
 
Perform reconnaissance with timing: 
netauto -i 192.168.69.10 -t5
 
Perform protocols, port and service scan: 
netauto -i 192.168.69.10 -p 40,60,80
                                                                                                                                                                                                                                           
```

# Results
The following results of these scans will produce NMAP directory and the rest of enumeration programs for each of the following ports through its name that will store and output all enumeration results of specified protocols through either -oN flag from NMAP or use tee to output the results into specified location 

## Reconnaissance
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

## Port and Service Scanning
```
Netauto
└── 192.168.69.10
    └── Protocols
        ├── DNS
        │   └── nmap
        │       ├── broadcast-dns-service-discovery.txt
        │       ├── dns-all.txt
        │       ├── dns-blacklist.txt
        │       ├── dns-cache-snoop.txt
        │       ├── dns-check-zone.txt
        │       ├── dns-client-subnet-scan.txt
        │       ├── dns-fuzz.txt
        │       ├── dns-ip6-arpa-scan.txt
        │       ├── dns-nsec-enum.txt
        │       ├── dns-nsec3-enum.txt
        │       ├── dns-nsid-extended.txt
        │       ├── dns-nsid.txt
        │       ├── dns-random-srcport.txt
        │       ├── dns-random-txid.txt
        │       ├── dns-recursion.txt
        │       ├── dns-service-discovery.txt
        │       ├── dns-srv-enum.txt
        │       ├── dns-update.txt
        │       ├── dns-zeustracker.txt
        │       └── dns-zone-transfer.txt
        ├── HTTP
        │   ├── CMSScan
        │   │   ├── http-cms.txt
        │   │   ├── http-cmseek.txt
        │   │   ├── http-joomscan.txt
        │   │   └── http-wpscan.txt
        │   ├── Firewall
        │   │   ├── http-wafw00f.txt
        │   │   └── http-whatwaf.txt
        │   ├── automatic_scanners
        │   │   ├── nikto
        │   │   │   └── http-nikto.txt
        │   │   ├── wapiti
        │   │   │   └── http-wapiti.txt
        │   │   │       ├── 192.168.69.10_05252024_1416.html
        │   │   │       ├── css
        │   │   │       │   ├── kube.min.css
        │   │   │       │   └── master.css
        │   │   │       ├── logo_clear.png
        │   │   │       └── report.html
        │   │   ├── webanalyze
        │   │   │   └── http-webanalyze.txt
        │   │   ├── webtech
        │   │   │   └── http-webtech.txt
        │   │   └── whatweb
        │   │       ├── http-whatweb-aggressive.txt
        │   │       ├── http-whatweb-extreme.txt
        │   │       ├── http-whatweb-stealthy.txt
        │   │       └── http-whatweb.txt
        │   └── nmap
        │       ├── http-auth.txt
        │       ├── http-devframework.txt
        │       ├── http-enum.txt
        │       ├── http-headers.txt
        │       ├── http-methods.txt
        │       ├── http-waf-detect.txt
        │       ├── http-wordpress-all.txt
        │       ├── http-wordpress-enum.txt
        │       └── http-wordpress-users.txt
        ├── SSH
        │   ├── nc
        │   │   ├── ssh-nc-nv.txt
        │   │   └── ssh-nc.txt
        │   ├── nmap
        │   │   ├── ssh-all.txt
        │   │   ├── ssh-auth-methods-default.txt
        │   │   ├── ssh-auth-methods.txt
        │   │   ├── ssh-hostkey.txt
        │   │   ├── ssh-publickey-acceptance.txt
        │   │   ├── ssh-run.txt
        │   │   └── ssh2-enum-algos.txt
        │   ├── ssh-audit
        │   │   └── ssh-audit.txt
        │   └── ssh-keyscan
        │       └── ssh-keyscan-public-key.txt
        └── ftp
            ├── ftp_nc.txt
            ├── ftp_nc_nv.txt
            ├── nc
            ├── nmap
            │   ├── ftp-all.txt
            │   ├── ftp-anon.txt
            │   ├── ftp-bounce.txt
            │   ├── ftp-libopie.txt
            │   ├── ftp-proftpd-backdoor.txt
            │   ├── ftp-syst.txt
            │   ├── ftp-vuln-all.txt
            │   └── ftp-vuln-cve2010-4221.txt
            └── openssl
                └── ftp-openssl.txt

```
