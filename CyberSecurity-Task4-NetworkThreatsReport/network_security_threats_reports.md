# Common Network Security Threats
## 📌 Introduction
Network security threats are more important today than ever because cybercrime has become a big business run by organized criminals. They use artificial intelligence (AI) and take advantage of world conflicts to launch advanced attacks on a massive scale. Companies now face more than 2,200 attacks every week, and fraud has become a bigger worry for business leaders than ransomware. Attackers use AI to create fake emails that look real, spread harmful software automatically, and find weaknesses in computer systems much faster than before. They are also attacking new industries like farming and hotels, not just the usual targets. The risks are greater because almost everything is connected our bank accounts, medical records, power grids, and even national security. One successful attack can cause huge money losses, steal people's identities, shut down businesses, and destroy public trust.
## DoS/DDoS Attacks

Attackers use botnets to send massive volumes of traffic to a target server, exhausting its resources (bandwidth, CPU, memory) until it can no longer respond to legitimate requests.
### Real-World Example
A 22-year-old Oregon man has been arrested on suspicion of operating “Rapper Bot,” a massive botnet used to power a service for launching distributed denial-of-service (DDoS) attacks against targets — including a March 2025 DDoS that knocked Twitter/X offline. The Justice Department asserts the suspect and an unidentified co-conspirator rented out the botnet to online extortionists, and tried to stay off the radar of law enforcement by ensuring that their botnet was never pointed at KrebsOnSecurity.(Krebs,2025)

### Impact of DDoS Attacks
Based on a research by Rao (2021), DDoS attacks can have severe consequences:
Loss of online transactions and potential business failure- Disruption of normal business operations
 - Government websites being taken down during protests or political conflicts
 - Ego-driven attacks where attackers boast about their capabilities
 - Financial gain for cybercriminals
 - Low barrier to entry, allowing even beginners to launch attacks using readily available tools.
### Mitigation Strategies
According to Rao (2021), network administrators can mitigate DDoS attacks using Cisco router configurations:
Method 1: ACL with Rate Limiting. This approach uses an Access Control List (ACL) to identify the attacker's IP address and applies rate limiting to restrict their traffic to 8000 bps. Legitimate users from other networks still get full access, although server response time may increase during an attack.
 Method 2: Class Map with Policy Map. This advanced Cisco feature uses Class Maps to segregate traffic based on parameters like source/destination addresses, ports, protocols, or even application-layer data (HTTP URLs, cookies). Policy Maps then apply Committed Access Rate (CAR) to limit the attacker's traffic. This method is more suitable for complex networks and Distributed Denial of Service scenarios with multiple attackers.
Method 3:Automatic SSH insertion. This is an advanced mitigation technique that uses automated shell scripts to defend against DDoS attacks without human intervention. Developed by Dr. Martin Reed at the University of Essex, this method employs the "Expect" command-line tool to establish a Secure Shell (SSH) connection with a Cisco router and insert Access Control List (ACL) or rate-limiting commands automatically. A logical loop in the script counts how many times an IP address repeats itself—any IP that exceeds a defined threshold (e.g., 10 connection attempts) is automatically added to the ACL and denied access to the server. This approach works continuously without manual updates, making it highly effective for real-time network environments where attacks need to be stopped immediately.
## 2. Man-in-the-middle attacks
A Man-in-the-Middle attack occurs when a hacker secretly gets between two people or systems that are communicating. Once in the middle, the attacker can listen to the conversation, steal information, or even change the messages being sent. This can result in stolen data, compromised login credentials, and unauthorized system access (Wolkstein, 2025).
### Real-world example 
In mid‑2024 and early 2025, telecoms in the U.S. including AT&T, Verizon, Lumen Technologies, and T-Mobile were targeted by a state‑linked group called Salt Typhoon. Attackers executed MITM-style intrusions deep into carrier networks, enabling interception of voice calls and location tracking without detection. It compromised sensitive communications across business and government sectors and is considered the largest telecom hack in U.S. history (Wolkstein, 2025).
### Impact of Man-in-the-middle attacks 
Man-in-the-Middle (MITM) attacks can have devastating consequences for both individuals and organizations. The most immediate impact is:
 
 - Data theft: where attackers steal sensitive information such as login credentials, credit card numbers, and confidential business communications. This often leads to financial losses through direct theft, fraudulent transfers, and costly incident response efforts. Stolen personal information can also result in identity theft, causing long-term damage to victims' credit and reputation. 
 - Erode customer trust: Damaging an organization's reputation and leading to loss of business. Organizations may face legal and regulatory consequences, including fines and lawsuits for failing to protect sensitive data.  (Wagner & Bryner, 2006; Wolkstein, 2025).
 ### Mitigation strategies 
 Based on Wolkstein (2025), organizations can defend against Man-in-the-Middle attacks using the following strategies:
 - Enforce End-to-End Encryption
End-to-end encryption ensures that data sent between clients and servers remains confidential throughout transmission. Only the intended endpoints can decrypt and access the information, making it far more difficult for attackers to read or manipulate intercepted data. 
 - Implement Multi-Factor Authentication (MFA):
Multi-factor authentication adds an extra layer of security by requiring users to provide two or more forms of verification before accessing critical systems. Even if attackers intercept usernames and passwords via a MITM attack, they will not be able to authenticate without the additional factors, such as time-based one-time passwords (TOTP), mobile push notifications, or hardware tokens. Implementing MFA should be mandatory for all sensitive systems, including administrative portals, financial services, and internal corporate resources. 
 - Continuous Monitoring, Detection, and Incident Response: 
Continuous monitoring of network traffic and user activity is critical for early detection of MITM attacks. Security tools such as intrusion detection systems (IDS), network intrusion prevention systems (NIPS), and security information and event management (SIEM) platforms can identify anomalies, suspicious patterns, and signs of traffic interception. Real-time alerts prompt incident response teams to investigate potential MITM scenarios before attackers can cause significant damage. In the event of a detected attack, organizations need a well-documented incident response plan that includes isolating affected systems, blocking malicious traffic, and revoking compromised credentials or sessions. Conducting a thorough post-incident analysis helps identify the root cause and strengthens defenses for the future.
## IP Spoofing 
IP spoofing is an attack method used to gain unauthorized access to a network. It exploits the fact that routers primarily examine the destination address to route traffic while largely ignoring the source address. The source address is only used by the destination machine when responding. In an IP spoofing attack, the intruder sends messages to a computer with forged packet headers, making them appear to come from a trusted system. The attacker's goal is to establish a connection that grants root access, allowing them to create a backdoor into the target system (Velasco, 2000).
### Real-world example 
One of the earliest documented IP spoofing attacks was carried out by Robert Morris, creator of the infamous Internet Worm. In 1989, Morris figured out how TCP generated sequence numbers and forged a TCP packet sequence. By spoofing the destination address, he was able to gain root access to his target system without needing a User ID or password (Velasco, 2000, p. 2).
### Impact of IP Spoofing 
According to Velasco (2000), the impacts of IP spoofing include:
 - System Manipulation: Attackers can load Trojan horses, modify data, and fully manipulate the compromised system
 - Blind Attacks: Attackers can impersonate trusted hosts and carry out attacks without seeing responses.
 - Unauthorized Access: Attackers can gain root access to target systems without a User ID or password
 - Backdoor Installation: Once compromised, attackers install backdoors for future access.
### Mitigation strategies 
1. Avoid Address-Based Authentication
Organizations should not rely solely on IP addresses to verify a user's identity. This can be achieved by disabling legacy Unix commands (r* commands) and removing trust files like .rhosts and /etc/hosts.equiv. Instead, remote users should be required to use more secure connection methods such as SSH, Telnet, or S/Key authentication (Velasco, 2000).
2. Encrypt All Network Traffic
Encrypting data transmitted across networks helps protect source and destination information from being intercepted or manipulated. When traffic is encrypted, even if an attacker intercepts it, they cannot easily read or modify the data (Velasco, 2000).
3. Use Random Initial Sequence Numbers
Implementing random initial sequence numbering makes it much harder for attackers to predict TCP sequence numbers. This prevents them from successfully forging packets and impersonating trusted hosts. This solution, first proposed by Bellovin in 1989, has since been adopted by many Unix-based operating systems (Velasco, 2000).
## DNS Poisoning/Spoofing
According to Fortinet(2026), DNS poisoning, also known as DNS cache poisoning, involves injecting false information into a DNS server's cache, which redirects users to malicious websites by providing incorrect IP addresses.
### Real-world example 
On April 24, 2015, attackers hijacked the DNS settings of the St. Louis Federal Reserve by manipulating routing configurations at their DNS vendor. This redirected visitors from the legitimate research website to fake pages that looked identical to the real site. Visitors who attempted to log in may have had their usernames and passwords stolen. The Federal Reserve confirmed the breach and required affected users to change their passwords (Krebs, 2015).
### Impacts of DNS Poisoning
According to Fortinet (2026), DNS poisoning can lead to major consequences.
 First, attackers can redirect users to phishing websites designed to steal sensitive information such as login credentials and financial data.
Second, victims may be sent to malicious sites that infect their systems with malware through drive-by downloads or Trojan installations.
Third, attackers can spoof security update sites, preventing computers from receiving critical patches and leaving them vulnerable to exploitation.
### Mitigation strategies 
For Website Owners and DNS Service Providers
1. DNS Spoofing Detection Tools: These tools scan DNS data before it reaches users, verifying that the information is accurate and legitimate, and blocking any corrupted or malicious data (Fortinet, 2026).
2. Domain Name System Security Extensions: DNSSEC adds a digital signature to DNS records, allowing systems to verify their authenticity and ensuring that users are not redirected to fraudulent websites (Fortinet, 2026).
3. End-to-End Encryption: Encrypting DNS traffic prevents attackers from intercepting and manipulating data in transit. Even if cybercriminals gain access to the DNS data, the encryption makes it unreadable and unusable (Fortinet, 2026).
For Endpoint Users
4. Avoid Suspicious Links: Users should type URLs directly into their browser rather than clicking on unfamiliar or suspicious links, as malicious links can lead to DNS attacks (Fortinet, 2026).
5. Regularly Scan for Malware: Regular antivirus scans help detect and remove malware that may have been accidentally downloaded through compromised websites, reducing the risk of further exploitation (Fortinet, 2026).
6. Flush DNS Cache: Flushing the DNS cache removes false or corrupted information stored on a device. This gives the system a fresh start and ensures DNS queries are processed correctly (Fortinet, 2026).
7. Use a Virtual Private Network (VPN): A VPN encrypts all data going to and from a device, making it difficult for cybercriminals to intercept or tamper with DNS information (Fortinet, 2026).

##  Table of comparison 
| Threat | Attack Vector | Who is at Risk | Difficulty to Execute | Ease of Mitigation |
| :--- | :--- | :--- | :--- | :--- |
| **DDoS Attacks** | Botnet traffic flood overwhelming servers and networks | Organizations with online services, e-commerce sites, government websites | Medium | Medium  |
| **MITM Attacks** | Intercepting communications between two parties | Public Wi-Fi users, financial institutions, government agencies | Medium | High  |
| **IP Spoofing** | Forging packet headers to impersonate trusted systems | Networks using address-based authentication | Medium-High  | Medium |
| **DNS Poisoning** | Injecting false information into DNS server caches | All internet users, organizations relying on DNS | High | High |
## Conclusion 
Network security threats like DDoS attacks, Man-in-the-Middle attacks, IP Spoofing, and DNS Poisoning are serious risks that can cause major harm to organizations. To stay protected, network administrators should follow these three key practices:
1. Use Multiple Layers of Security:No single defense is enough. A combination of firewalls, encryption, and monitoring provides better protection against different types of attacks.
2. Always Use Encryption and Strong Authentication :Encryption keeps data safe during transmission, and multi-factor authentication makes it harder for attackers to access systems even if they steal passwords
3. Monitor Networks and Have a Response Plan: Regular monitoring helps detect attacks early. A clear incident response plan ensures that when an attack happens, the team can act quickly to isolate systems, block threats, and recover with minimal damage.

## References 

1. Cybersecurity and Infrastructure Security Agency (CISA). (2021). Zero Trust Maturity Model, Pre-Decisional Draft, Version 1.0. U.S. Department of Homeland Security. https://www.cisa.gov/sites/default/files/publications/CISA%20Zero%20Trust%20Maturity%20Model_Draft.pdf 
2. Fortinet. (2026). What Is DNS Poisoning? Fortinet Cyber Glossary. https://www.fortinet.com/resources/cyberglossary/dns-poisoning 
3. Krebs, B. (2015, May 18). St. Louis Federal Reserve Suffers DNS Breach. KrebsOnSecurity. https://krebsonsecurity.com/2015/05/st-louis-federal-reserve-suffers-dns-breach/ 
4. Krebs, B. (2025, August 19). Oregon Man Charged in 'Rapper Bot' DDoS Service. KrebsOnSecurity.  
https://krebsonsecurity.com/2025/08/oregon-man-charged-in-rapper-bot-ddos-service/
5. Rao, S. (2021). Denial of Service attacks and mitigation techniques: Real time implementation with detailed analysis [White Paper]. SANS Institute Reading Room. https://sansorg.egnyte.com/dl/G67634mgDWMK 

7. Velasco, V. (2000, November 21). Introduction to IP Spoofing. SANS Institute Reading Room. https://sansorg.egnyte.com/dl/Mjb4FfXCJdy8 
8. Wagner, R., & Bryner, J. (2006). Address Resolution Protocol Spoofing and Man-in-the-Middle Attacks. SANS Institute Reading Room. https://sansorg.egnyte.com/dl/FK99HyDf94qH 
9. Wolkstein, E. (2025, September 10). 7 Types of Man in the Middle Attacks and 5 Real World Examples https://seraphicsecurity.com/learn/website-security/7-types-of-man-in-the-middle-attacks-and-5-real-world-examples/ 
