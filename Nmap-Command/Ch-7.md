## TCP Scan

### TCP ack Scan

```
nmap -sA scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 11:37 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00024s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
All 1000 scanned ports on scanme.nmap.org (45.33.32.156) are in ignored states.
Not shown: 1000 unfiltered tcp ports (reset)

Nmap done: 1 IP address (1 host up) scanned in 4.20 seconds

```

### TCP Stealth scan

In a TCP stealth scan, the three-way handshake is not completed. Nmap sends a `SYN` packet, receives a `SYN/ACK` in response, and then sends a `RESET flag` to the destination. The stealth scan can be easily detected by the blue team because its window size is always set to `1024 bytes`.

```
nmap -sS -p 22 scanme.nmap.org
Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 11:39 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00038s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT   STATE    SERVICE
22/tcp filtered ssh

Nmap done: 1 IP address (1 host up) scanned in 0.38 seconds
```

#### Pcap OP:-

![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2011.42.05%20AM.png)

### TCP connect scan

In a TCP connect scan, the three-way handshake is completed, and the window value is set to a legitimate value. However, one issue is that the scan gets logged at the destination end.

```
nmap -sT -p 22 scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 12:09 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00036s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT   STATE    SERVICE
22/tcp filtered ssh

Nmap done: 1 IP address (1 host up) scanned in 0.31 seconds
```

![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2012.09.09%20PM.png)

### TCP Xmas scan

In this scan `nmap`  set `fin, urg, psh flag to 1` . 

```
sudo nmap -sX scanme.nmap.org 

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 12:19 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00055s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
All 1000 scanned ports on scanme.nmap.org (45.33.32.156) are in ignored states.
Not shown: 1000 open|filtered tcp ports (no-response)

Nmap done: 1 IP address (1 host up) scanned in 5.41 seconds
```
![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2012.20.53%20PM.png)

### TCP fin scan:

In this scan `nmap`  set `fin flag to 1` . 

```
sudo nmap -sF scanme.nmap.org

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 12:23 IST
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.00033s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
All 1000 scanned ports on scanme.nmap.org (45.33.32.156) are in ignored states.
Not shown: 1000 open|filtered tcp ports (no-response)

Nmap done: 1 IP address (1 host up) scanned in 4.18 seconds
```

![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2012.23.37%20PM.png)

