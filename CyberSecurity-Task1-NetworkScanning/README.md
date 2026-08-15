# Network scanning 

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
#### step 1:update the package list to make sure you get the latest version 
sudo apt-get update
#### Step 2: install Nmap using package manager 
sudo apt-get install nmap -y
##### step 3: verify you installed the correct Nmap version
nmap --version
### Scan Command Used
nmap -sV localhost -oN nmap_scan_results.txt


### Port Analysis
## Scan Results

| Port | State | Service | Version | Security Risk |
| :--- | :--- | :--- | :--- | :--- |
| 22 | Open | SSH | OpenSSH 9.6p1 Ubuntu | Medium |
| 900 | Open | Unknown | Google Metadata Service |  Low |
| 981 | Open | HTTP | Golang net/http server |  Medium |
| 2222 | Open | SSH | OpenSSH 9.6p1 Ubuntu |  Medium |

#### Port 22 – SSH (Secure Shell)
This service allows secure remote login and command execution on the server. It is commonly used by system administrators to manage servers from a distance. The risk is medium because while SSH is secure by design, weak passwords, outdated versions, or allowing root login can make it vulnerable to brute-force attacks.
#### Port 900 – Google Metadata Service 
This is an internal Google Cloud service that provides configuration information to the Cloud Shell instance. It is not accessible from the outside internet. The risk is low because it is only used within Google's infrastructure and does not expose sensitive data to external users.
#### Port 981 – HTTP (Go Web Server): 
This port is running a web server built with the Go programming language. It serves web content over HTTP, which is unencrypted. The risk is medium because any data sent to or from this server can be intercepted by an attacker, making it unsafe for transmitting sensitive information like passwords or personal data.
#### Port 2222 – SSH (Alternate Port):
This is another SSH service running on a non-standard port. Some administrators change the default SSH port to avoid automated scans. However, this is considered "security through obscurity" and does not replace proper security practices. The risk is medium and the same recommendations for Port 22
