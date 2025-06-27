 ElevateLabs-Task1
nmap-local-network-scan-task
---
Task 1: Scan Your Local Network for Open Ports

  Author
**Sakshi Dhananjay Kamble**  
M.Sc. Cybersecurity, Mumbai University  
June 2025  
Elevate Labs
---
 Objective

To learn and perform basic and advanced port scanning using Nmap on a local Ubuntu-based system by:
- Installing and verifying Nmap
- Setting up a test HTTP server
- Performing various types of port scans
- Saving output in multiple formats
- Understanding scan results and implications

---
Commands Used

Install Nmap
sudo apt update
sudo apt install nmap -y

---
Start HTTP Server

mkdir -p ~/project/http-server
cd ~/project/http-server
echo "<html><body><h1>Welcome to the Nmap Lab</h1></body></html>" > index.html
python3 -m http.server 8000

---
Perform Scans

nmap -sT -p 8000 localhost               # Basic TCP scan
nmap -sV -p 8000 localhost               # Service version detection
nmap localhost                           # Top 1000 ports
nmap -p- localhost                       # All ports
nmap -p 1-1000 localhost                 # Specific port range

---
Save Outputs

nmap -oN normal_output.txt localhost
nmap -oX xml_output.xml localhost
nmap -oG grepable_output.txt localhost

---

Screenshots attached in Documents

---

Interview Questions Covered
---

What is an open port?

TCP vs UDP scanning

How Nmap performs SYN scans

Common port vulnerabilities

Role of firewalls

How Wireshark complements scanning

---

Disclaimer
Use Nmap responsibly and only on systems you have permission to scan.

Useful Links
Nmap Official Site

Wireshark

---
