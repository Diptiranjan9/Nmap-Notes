## Nmap scan for specific port 

### These scan are by default using `tcp`.

- Scan for specific port

```
nmap -p 80,443 scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 19:59 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.076s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT    STATE  SERVICE
80/tcp  open   http
443/tcp closed https

Nmap done: 1 IP address (1 host up) scanned in 1.41 seconds
```

- Scan port range

```
nmap -p 1-100 scanme.nmap.org 

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:00 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.31s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 97 closed tcp ports (reset)
PORT   STATE    SERVICE
22/tcp open     ssh
25/tcp filtered smtp
80/tcp open     http

Nmap done: 1 IP address (1 host up) scanned in 1.91 seconds
```


### For `udp` scan use `-sU` option


```
nmap -p 22,53,80 -sU scanme.nmap.org

op:- 

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:06 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00047s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT   STATE         SERVICE
22/udp open|filtered ssh
53/udp open|filtered domain
80/udp open|filtered http

Nmap done: 1 IP address (1 host up) scanned in 1.72 seconds
```

```
nmap -p 22,53,80 -sU 127.0.0.1

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-26 20:06 IST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000020s latency).

PORT   STATE  SERVICE
22/udp closed ssh
53/udp open   domain
80/udp closed http

Nmap done: 1 IP address (1 host up) scanned in 0.15 seconds
```
