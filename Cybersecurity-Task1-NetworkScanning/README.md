# Network scanning 

## Scan Results

| Port | State | Service | Version | Security Risk |
| :--- | :--- | :--- | :--- | :--- |
| 22 | Open | SSH | OpenSSH 9.6p1 Ubuntu | Medium |
| 900 | Open | Unknown | Google Metadata Service |  Low |
| 981 | Open | HTTP | Golang net/http server |  Medium |
| 2222 | Open | SSH | OpenSSH 9.6p1 Ubuntu |  Medium |
## What is nmap?
Network Mapper(Nmap) is a free, open-source tool used for network discovery and security auditing.
## Why Network scanning matters?
Network scanning is important because it helps organizations find potential security problems before attackers do.
By regularly scanning their networks, administrators can discover unauthorized services, detect open ports that could be entry points for hackers, and keep track of all devices connected to their network.
Without scanning, vulnerabilities can go unnoticed and be exploited by cybercriminals.
## Ethical Use Guidelines
Network scanning must always be done responsibly and ethically. You should only scan systems that you own or have explicit written permission to scan.
Scanning external networks, public Wi-Fi, or production systems without authorization is illegal and unethical.
For this task, I only scanned my own Cloud Shell instance (localhost), which is completely safe and allowed.

## Installation steps
step 1: update the package list to make sure you get the latest version 
sudo apt-get update
Step 2: install Nmap using package manager 
sudo apt-get install nmap -y
step 3: verify you installed the correct Nmap version
nmap --version
### Scan Command Used
nmap -sV localhost -oN nmap_scan_results.txt
