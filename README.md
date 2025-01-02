# The-Complete-Nmap-Guide
A comprehensive resource covering everything about Nmap—from basic commands to advanced scanning techniques. Perfect for beginners and professionals seeking to master network exploration and security auditing with Nmap.

**Targets:**
Scan a single IP: nmap 192.168.1.1
Scan specific IPs: nmap 192.168.1.1 192.168.1.2
Scan a range: nmap 192.168.1.1-254
Scan a domain: nmap scanme.nmap.org
Scan using CIDR: nmap 192.168.1.0/24
Scan from a file: nmap -iL targets.txt
Scan random hosts: nmap -iR 100
Exclude hosts: nmap --exclude 192.168.1.1

**Scan Types:**
TCP SYN Scan (default): nmap 192.168.1.1
TCP Connect Scan: nmap -sT 192.168.1.1
UDP Scan: nmap -sU 192.168.1.1
Stealth Scans (use with caution): nmap -sS, -sF, -sX

**Host Discovery:**
List only targets: nmap 192.168.1.1-3 -sL
Disable port scan: nmap 192.168.1.1/24 -sn
TCP ACK Scan (specify ports): nmap -PA 192.168.1.1-5

**Port Scanning:**
Scan specific port: nmap 192.168.1.1 -p 80
Scan a port range: nmap 192.168.1.1 -p 21-100
Scan multiple ports (TCP/UDP): nmap 192.168.1.1 -p U:53,T:21-25,80
Scan all ports: nmap 192.168.1.1 -p-
Scan by service name: nmap 192.168.1.1 -p http,https
Fast Scan (limited ports): nmap -F 192.168.1.1
Top Ports Scan: nmap 192.168.1.1 --top-ports 2000

**Service & Version Detection:**
Attempt service version detection: nmap 192.168.1.1 -sV
Increase version detection intensity: nmap -sV --version-intensity 8
Enable light mode (faster, less accurate): nmap -sV --version-light
Enable all intensity levels: nmap -sV --version-all

**OS Detection:**
Detect OS using TCP/IP stack fingerprinting: nmap 192.168.1.1 -O
More aggressive OS detection: nmap -O --osscan-limit 192.168.1.1
Set max OS detection tries: nmap -O --max-os-tries 1 192.168.1.1

**Output:**
Save normal output to file: nmap 192.168.1.1 -oN normal.txt
Save XML output to file: nmap 192.168.1.1 -oX xml.txt
Show open ports only: nmap 192.168.1.1 --open

**Timing and Performance:**
-T0 to -T5: Speed profiles (0 = slowest, 5 = fastest): nmap -T4 192.168.1.1
--max-rate 100: Limit probes per second
