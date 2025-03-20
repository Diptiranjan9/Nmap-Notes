## UDP Scan

```
nmap -sU -p 19,53,123 scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 12:29 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.077s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT    STATE         SERVICE
19/udp  open|filtered chargen
53/udp  open|filtered domain
123/udp open          ntp

Nmap done: 1 IP address (1 host up) scanned in 3.10 seconds

```
