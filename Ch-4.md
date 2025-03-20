## Top 5 scan command

### Ping scan:-

```
nmap -sn 192.168.245.10/24 

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:17 IST
Nmap scan report for 192.168.245.1
Host is up (0.00032s latency).
MAC Address: 9E:58:84:D3:70:65 (Unknown)
Nmap scan report for 192.168.245.2
Host is up (0.00037s latency).
MAC Address: 00:50:56:E2:CC:64 (VMware)
Nmap scan report for 192.168.245.254
Host is up (0.00049s latency).
MAC Address: 00:50:56:F4:93:86 (VMware)
Nmap scan report for 192.168.245.10
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 1.92 seconds
```

### Top 20 port scan :-

```
nmap --top-port 20 scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:44 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.36s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT     STATE    SERVICE
21/tcp   closed   ftp
22/tcp   open     ssh
23/tcp   closed   telnet
25/tcp   filtered smtp
53/tcp   closed   domain
80/tcp   open     http
110/tcp  closed   pop3
111/tcp  closed   rpcbind
135/tcp  filtered msrpc
139/tcp  filtered netbios-ssn
143/tcp  closed   imap
443/tcp  closed   https
445/tcp  filtered microsoft-ds
993/tcp  closed   imaps
995/tcp  closed   pop3s
1723/tcp closed   pptp
3306/tcp closed   mysql
3389/tcp closed   ms-wbt-server
5900/tcp closed   vnc
8080/tcp closed   http-proxy

Nmap done: 1 IP address (1 host up) scanned in 8.21 seconds
```


### OS scan:-

```
nmap -O 192.168.245.1   

op:- 

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:19 IST
Nmap scan report for 192.168.245.1
Host is up (0.00049s latency).
Not shown: 999 filtered tcp ports (no-response)
PORT   STATE SERVICE
22/tcp open  ssh
MAC Address: 9E:58:84:D3:70:65 (Unknown)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Apple iOS 15.7 (Darwin 21.7.0) (93%), Apple macOS 11 (Big Sur) - 13 (Ventura) or iOS 16 (Darwin 20.6.0 - 22.4.0) (93%), Apple macOS 11 (Big Sur) (Darwin 20.6.0) (90%), Apple iOS 15.0 - 15.6 (Darwin 21.1.0 - 21.6.0) (88%), Apple macOS 10.13 (High Sierra) - 10.15 (Catalina) or iOS 11.0 - 14.3 (Darwin 17.0.0 - 20.2.0) (87%), Apple macOS 10.14 (Mojave) (Darwin 18.7.0) (87%), FreeBSD 11.3-RELEASE (87%), FreeBSD 12.0-RELEASE - 12.1-RELEASE (87%), FreeBSD 12.2-RELEASE - 13.0-RELEASE (87%), FreeBSD 13.0-RELEASE (87%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 1 hop

OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.10 seconds
```

### OS, Version, Trace Scan (aggressive scanning):-

```
nmap -A 192.168.245.1

op:- 

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:22 IST
Nmap scan report for 192.168.245.1
Host is up (0.000085s latency).
All 1000 scanned ports on 192.168.245.1 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
MAC Address: 9E:58:84:D3:70:65 (Unknown)
Too many fingerprints match this host to give specific OS details
Network Distance: 1 hop

TRACEROUTE
HOP RTT     ADDRESS
1   0.09 ms 192.168.245.1

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 29.18 seconds
```

```
nmap -A 192.168.245.10

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:23 IST
Nmap scan report for 192.168.245.10
Host is up (0.000056s latency).
Not shown: 999 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
5222/tcp open  ssh     OpenSSH 9.9p1 Debian 3 (protocol 2.0)
| xmpp-info: 
|   STARTTLS Failed
|   info: 
|     compression_methods: 
|     errors: 
|       (timeout)
|     unknown: 
|     xmpp: 
|     features: 
|     capabilities: 
|_    auth_mechanisms: 
| ssh-hostkey: 
|   256 d2:03:75:c2:04:bb:00:e8:6b:e9:6a:5b:ff:f1:70:71 (ECDSA)
|_  256 01:e0:04:7f:0f:7f:5d:16:4a:25:7d:27:79:df:19:5b (ED25519)
Device type: general purpose
Running: Linux 2.6.X|5.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:5 cpe:/o:linux:linux_kernel:6
OS details: Linux 2.6.32, Linux 5.0 - 6.2
Network Distance: 0 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 41.68 seconds
```


### TCP Stealth scan:-

This `-sS` option is used to avoid sending the 3-way handshake `ACK`; it directly sends a `RST`.

```
nmap -sS -p 80 scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:58 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00086s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT   STATE    SERVICE
80/tcp filtered http

Nmap done: 1 IP address (1 host up) scanned in 0.92 seconds
```

