## Nmap scan for IP range

#### NMAP Scan for single subnet

```
nmap 192.168.245.10/24

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 19:02 IST
Nmap scan report for 192.168.245.1
Host is up (0.00036s latency).
Not shown: 999 filtered tcp ports (no-response)
PORT   STATE SERVICE
22/tcp open  ssh
MAC Address: 9E:58:84:D3:70:65 (Unknown)

Nmap scan report for 192.168.245.2
Host is up (0.00070s latency).
All 1000 scanned ports on 192.168.245.2 are in ignored states.
Not shown: 1000 closed tcp ports (reset)
MAC Address: 00:50:56:E2:CC:64 (VMware)

Nmap scan report for 192.168.245.254
Host is up (0.00055s latency).
All 1000 scanned ports on 192.168.245.254 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
MAC Address: 00:50:56:F4:93:86 (VMware)

Nmap scan report for 192.168.245.10
Host is up (0.0000060s latency).
Not shown: 999 closed tcp ports (reset)
PORT     STATE SERVICE
5222/tcp open  xmpp-client

Nmap done: 256 IP addresses (4 hosts up) scanned in 8.27 seconds
```

#### NMAP scan for two subnet

```
nmap 192.168.245.10/24 10.10.10.0/24
```

#### Nmap scan for ip range

```
nmap 192.168.245.1-10
```