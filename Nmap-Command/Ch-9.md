## OS Fingerprint

```
nmap -O scanme.nmap.org -v

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 13:56 IST
Initiating Ping Scan at 13:56
Scanning scanme.nmap.org (45.33.32.156) [4 ports]
Completed Ping Scan at 13:56, 0.03s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 13:56
Completed Parallel DNS resolution of 1 host. at 13:56, 0.00s elapsed
Initiating SYN Stealth Scan at 13:56
Scanning scanme.nmap.org (45.33.32.156) [1000 ports]
Discovered open port 80/tcp on 45.33.32.156
Discovered open port 22/tcp on 45.33.32.156
Discovered open port 9929/tcp on 45.33.32.156
Discovered open port 9929/tcp on 45.33.32.156
Discovered open port 31337/tcp on 45.33.32.156
Completed SYN Stealth Scan at 13:56, 21.26s elapsed (1000 total ports)
Initiating OS detection (try #1) against scanme.nmap.org (45.33.32.156)
Retrying OS detection (try #2) against scanme.nmap.org (45.33.32.156)
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.28s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 992 closed tcp ports (reset)
PORT      STATE    SERVICE
22/tcp    open     ssh
25/tcp    filtered smtp
80/tcp    open     http
135/tcp   filtered msrpc
139/tcp   filtered netbios-ssn
445/tcp   filtered microsoft-ds
9929/tcp  open     nping-echo
31337/tcp open     Elite
Aggressive OS guesses: Actiontec MI424WR-GEN3I WAP (96%), DD-WRT v24-sp2 (Linux 2.4.37) (95%), Linux 3.2 (93%), Microsoft Windows XP SP3 or Windows 7 or Windows Server 2012 (93%), Linux 4.4 (91%), Microsoft Windows XP SP3 (91%), BlueArc Titan 2100 NAS device (87%)
No exact OS matches for host (test conditions non-ideal).
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: Incremental

Read data files from: /usr/share/nmap
OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 29.08 seconds
           Raw packets sent: 1269 (59.136KB) | Rcvd: 1243 (50.836KB)
```

## Version Scan

```
nmap -sV scanme.nmap.org 

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 14:57 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.42s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 992 closed tcp ports (reset)
PORT      STATE    SERVICE      VERSION
22/tcp    open     ssh          OpenSSH 6.6.1p1 Ubuntu 2ubuntu2.13 (Ubuntu Linux; protocol 2.0)
25/tcp    filtered smtp
80/tcp    open     http         Apache httpd 2.4.7 ((Ubuntu))
135/tcp   filtered msrpc
139/tcp   filtered netbios-ssn
445/tcp   filtered microsoft-ds
9929/tcp  open     nping-echo   Nping echo
31337/tcp open     tcpwrapped
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 26.50 seconds
```

[!Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%203.03.39%20PM.png)

[!Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%203.07.19%20PM.png)

