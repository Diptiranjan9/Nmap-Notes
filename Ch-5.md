## Local network scan

In a local network scan within the same subnet, Nmap uses `ARP`. When it finds a host that responds to an `ARP request`, it sends a `TCP three-way handshake` packet.

```
nmap -sn 192.168.245.10/24 

op:-

Starting Nmap 7.95 ( https://nmap.org ) at 2025-02-27 10:42 IST
Nmap scan report for 192.168.245.1
Host is up (0.00014s latency).
MAC Address: 9E:58:84:D3:70:65 (Unknown)
Nmap scan report for 192.168.245.2
Host is up (0.00024s latency).
MAC Address: 00:50:56:E2:CC:64 (VMware)
Nmap scan report for 192.168.245.254
Host is up (0.00030s latency).
MAC Address: 00:50:56:FF:AF:C8 (VMware)
Nmap scan report for 192.168.245.10
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 2.02 seconds
```

#### Pcap OP:-

![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2010.44.33%20AM.png)

![Diagram](https://github.com/Diptiranjan9/Nmap-Notes/blob/main/pcap/Screenshot%202025-02-27%20at%2010.46.45%20AM.png)
