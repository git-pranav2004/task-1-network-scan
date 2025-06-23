 Task 1 – Scan Your Local Network for Open Ports

Internship: Elevate Labs – Cybersecurity  
Objective: Learn how to perform a basic network reconnaissance using Nmap and Wireshark to discover open ports, understand exposure, and identify potential risks.

---

 Tools Used

- Nmap – For scanning open ports using TCP SYN scans
- Wireshark – For capturing and analyzing live network packets

---

 Steps Performed

 1. Determined My Local Network
- Used `ipconfig` to find local IP: `192.168.56.x`
- Determined subnet: `192.168.56.0/24`

 2. Performed TCP SYN Scan using Nmap
nmap -sS 192.168.56.0/24 -oN scan_output.txt

3. Captured Packets Using Wireshark
Started Wireshark before running the scan.
Selected the active Wi-Fi interface.
Applied filter:
  tcp.flags.syn==1 && tcp.flags.ack==0
Observed SYN packets sent by Nmap and responses from devices.

Key Scan Findings
IP Address	      Open Ports	                  Services
192.168.56.1	   135, 139, 445	    MSRPC, NetBIOS-SSN, Microsoft-DS
192.168.56.100	       22	                         SSH


This file is **self-contained** — no links or external files required. Just update the screenshot filenames if needed and paste it into your GitHub repo as `README.md`.
