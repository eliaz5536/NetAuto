![automated_network_enumerator](https://github.com/eliaz5536/NetAuto/assets/5835036/55eafde0-f387-49fa-913a-bb4436bb797e)

# Demos
## Reconnaissance
[![asciicast](https://asciinema.org/a/ow43LeBg337iVj2zR5NOSINuD.svg)](https://asciinema.org/a/ow43LeBg337iVj2zR5NOSINuD)

## Port Enumeration
[![asciicast](https://asciinema.org/a/9E0OLYfkxGyrFROLYjASIZeM5.svg)](https://asciinema.org/a/9E0OLYfkxGyrFROLYjASIZeM5)

# NetAuto
NetAuto is a customizable network reconnaissance tool that automates enumeration of services, protocols and ports, suitable network scanning and penetration testing practices.

# Requirements
Your machine must be up-to-date in order to install the latest available packages
```
sudo apt-get update
```

If you want to install third-party tools to be installed in your system, execute this following command:
```
sudo apt-get install python python2 python3 python3-pip pip pipx
```

The tools that are utilized for enumeration requires installation of the following from the table:
| [Nmap](https://nmap.org/)         | OpenSSL          | Netcat             | snmpwalk   | snmp-check    | finger                |
|--------------|------------------|--------------------|------------|---------------|-----------------------|
| ntpq         | [impacket-rpcdump](https://github.com/fortra/impacket/tree/master) | [rpcdump](https://github.com/fortra/impacket/tree/master)            | [rpcmap](https://github.com/fortra/impacket/tree/master)     | [IOXIDResolver](https://github.com/mubix/IOXIDResolver) | nmblookup             |
| [nbtscan](https://github.com/charlesroelli/nbtscan)      | [enum4linux](https://github.com/CiscoCXSecurity/enum4linux)       | [enum4linux-ng](https://github.com/cddmp/enum4linux-ng)      | rpcclient  | [netexec](https://github.com/Pennyw0rth/NetExec)       | [smbmap](https://github.com/ShawnDEvans/smbmap)                |
| [crackmapexec](https://github.com/byt3bl33d3r/CrackMapExec) | [smbclient](https://github.com/fortra/impacket/tree/master)        | [impacket-looksupid](https://github.com/fortra/impacket/tree/master) | [IKE-Scan](https://github.com/royhills/ike-scan)   | [PRET](https://github.com/RUB-NDS/PRET)          | [rsync](https://github.com/RsyncProject/rsync)                 |
| rpcinfo      | [spose](https://github.com/aancw/spose)            | svn                | [SIETpy3](https://github.com/Sab0tag3d/SIETpy3)    | OpalOPC       | [DockerRegistryGrabber](https://github.com/Syzik/DockerRegistryGrabber) |
| [Nikto](https://github.com/sullo/nikto)        | [WhatWeb](https://github.com/urbanadventurer/WhatWeb)          | [WebTech](https://github.com/ShielderSec/webtech)            | [WebAnalyze](https://github.com/rverton/webanalyze) | [Wapiti](https://github.com/wapiti-scanner/wapiti)        | [wafw00f](https://github.com/EnableSecurity/wafw00f)              |
| [WhatWaf](https://github.com/Ekultek/WhatWaf)      | [CMSMap](https://github.com/dionach/CMSmap)           | [WPScan](https://github.com/wpscanteam/wpscan)             | [Joomscan](https://github.com/OWASP/joomscan)   | [CMSeeK](https://github.com/Tuhinshubhra/CMSeeK)        |                       |

The following commands used in this script can be accessible from such resources such as [hacktricks](https://book.hacktricks.xyz/), [infrastructure](https://infra.newerasec.com/), [0xffsec](https://0xffsec.com/handbook/) & [exploit-notes](https://exploit-notes.hdks.org/).

It is recommended that you install the following tools on **Debian** based distribution machine (_ParrotOS_ & _Kali Linux_) for the ease of installing third-party tools.

# Installation
```
# Clone the following repository
git clone https://github.com/eliaz5536/netauto.git # Clone repository

# Access the repository and change file permission of the script to be executable
chmod +x netauto 

# Launch NetAuto
./netauto 
```

```
./netauto -i <TARGET_HOST> -p <TARGET_PORTS>
```

# Usage 
It is recommended that you run sudo on this script since it requires specific permissions to execute Nmap commands.

```
Network Enumeration Automator with Nmap
 
Usage: Netauto -i <host> [options]
 
Options:
  -h, --help                      Help & Usage
  -i, --ip                        Specify target host
  -p, --ports                     Scan ports of target host
  -t, --timing                    Specify minrate option
  -m, --mode                      Specify scan mode
  -o, --output                    Output destination
 
Timing minrate options:
  0                       Paranoid
  1                       Sneaky
  2                       Polite
  3                       Normal (Default)
  4                       Aggressive
  5                       Insane
 
Mode options: 
 recon                    Recon Scan
 tcp                      TCP Scan
 udp                      UDP Scan
 script                   Script Scan
 vuln                     Vulnerability Scan                                                                                                                                                                                                                                        
```

# Examples
The following will produce output directories for each of the selected ports which that will output all enumeration scans.
## Reconnaissance Output Directory
```
Netauto
└── XXX.XXX.XX.XX
    └── Default
        ├── tcp.nmap
        ├── aggressive.nmap
        ├── port.nmap
        ├── script.nmap
        ├── stealth.nmap
        └── vuln.nmap
```

## Port Enumeration Output Directory
```
Netauto
└── XXX.XXX.XX.XX
    └── Protocols
        └── SSH
            ├── nc
            │   ├── nc-nv.txt
            │   └── nc.txt
            ├── nmap
            │   ├── all.nmap
            │   ├── auth-methods-default.nmap
            │   ├── auth-methods-root.nmap
            │   ├── auth-methods.nmap
            │   ├── enum-algos.nmap
            │   ├── hostkey.nmap
            │   ├── publickey-acceptance.nmap
            │   └── run.nmap
            ├── ssh-audit
            │   └── ssh-audit.txt
            └── ssh-keyscan
                └── rsa.txt
```
