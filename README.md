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
![image](https://github.com/user-attachments/assets/43ffed98-02b1-4f7d-8440-f4e70b2292e2)
![image](https://github.com/user-attachments/assets/cb03c952-7b5e-4886-99f3-5d23eb0dc7a5)
![image](https://github.com/user-attachments/assets/93abcf1b-28ac-4100-9de8-90013ffe04e8)
![image](https://github.com/user-attachments/assets/f039608b-1ad8-41c8-9752-b1ec46f597c5)
![image](https://github.com/user-attachments/assets/3d67667a-6e6e-4f48-a14d-39530c5a9034)
![image](https://github.com/user-attachments/assets/bb82474d-89fd-48ca-afeb-19ced679548f)
![image](https://github.com/user-attachments/assets/74a97f26-e6f1-4e55-9570-706a6f3569f6)
![image](https://github.com/user-attachments/assets/78e1dcaf-cb58-4c97-b324-48af7afbf665)
![image](https://github.com/user-attachments/assets/457a480a-f520-40f6-94a6-7913d67f4d74)
![image](https://github.com/user-attachments/assets/ef18c468-5818-4c50-9f12-7e8a20aaec23)
![image](https://github.com/user-attachments/assets/21e83408-6628-4642-96cb-a45c954a5183)
![image](https://github.com/user-attachments/assets/882eddae-5f23-42aa-a7d6-08f1d488418a)
![image](https://github.com/user-attachments/assets/8b69e812-d1da-4d8b-bfcd-0a6eb623afa7)
![image](https://github.com/user-attachments/assets/456b6c1a-dc6c-4056-b59e-950bdc0fab31)

---

