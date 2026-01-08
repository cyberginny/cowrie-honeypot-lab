# Cowrie SSH Honeypot Lab  
*Cybersecurity Project*

This project demonstrates the deployment of a **Cowrie SSH honeypot** in a controlled lab environment, along with **attack simulation, network traffic capture, and log analysis**.  
The goal is to observe real-world attacker behavior and gain hands-on blue-team experience.

---

##  Tools & Technologies
- Cowrie SSH Honeypot  
- Ubuntu / Debian (Honeypot VM)  
- Kali Linux (Attacker VM)  
- Nmap  
- Hydra  
- Wireshark  
- tcpdump  
- jq  

---

##  Project Structure
- `README.md` – Project documentation and analysis  
- `honeycowrie_installation.sh` – Honeypot setup and attack simulation commands  
- `screenshots/` – Evidence of honeypot activity, attacks, and analysis  

---

##  Lab Overview
The lab is divided into the following stages:

1. Environment setup and honeypot deployment  
2. Network reconnaissance and service enumeration  
3. Simulated SSH brute-force and enumeration attacks  
4. Network traffic capture and inspection  
5. Honeypot log analysis and attacker behavior review  

---

##  Screenshots

### Cowrie Honeypot Running
Shows the Cowrie service successfully initialized and running.
![Cowrie Status](screenshots/cowrie-status.png)

### SSH Brute-Force Attack (Hydra)
Demonstrates automated SSH credential attacks against the honeypot.
![Hydra Attack](screenshots/hydra-attack.png)

### Network Traffic Capture (Wireshark)
Captured SSH traffic on the honeypot port during active attacks.
![Wireshark Capture](screenshots/wireshark.png)

### Cowrie Log Analysis
Review of authentication attempts recorded by Cowrie.
![Cowrie Logs](screenshots/cowrie-logs.png)

---

##  Case Study: SSH Attack Detection Using Cowrie Honeypot

### Problem
SSH services are a frequent target for brute-force and credential-stuffing attacks.  
Standard system logs often provide limited insight into attacker behavior and techniques.

---

### Objective
To deploy an SSH honeypot that mimics a real server, capture attacker interactions, and analyze authentication attempts and network traffic patterns.

---

### Approach
- Deployed Cowrie SSH honeypot on an isolated Ubuntu virtual machine  
- Used Kali Linux to simulate realistic attacker activity  
- Conducted network reconnaissance using Nmap  
- Performed SSH brute-force attacks using Hydra  
- Captured traffic with tcpdump and analyzed packets in Wireshark  
- Parsed structured Cowrie JSON logs using jq  

---

### Results
- Captured multiple failed and successful SSH login attempts  
- Identified common usernames and weak password patterns  
- Observed attacker behavior without risking a production system  
- Correlated honeypot logs with captured network traffic  

---

### Key Takeaways
- Honeypots provide high-quality threat intelligence  
- SSH remains a highly targeted attack surface  
- Log analysis is essential for blue-team and SOC operations  
- Network traffic analysis complements application-level logs  

---

### Future Improvements
- Forward logs to an ELK or Splunk stack  
- Deploy multiple honeypots with different services  
- Implement alerting for successful authentication attempts  

---

## Disclaimer
This project is for **educational and ethical cybersecurity research only**.  
Do **not** deploy honeypots on production or unauthorized networks.
