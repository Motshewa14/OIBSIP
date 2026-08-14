# Social Engineering Attacks
Social engineering is a category of cyberattack that targets human psychology rather than technology. It relies on manipulation to trick individuals into revealing confidential information, granting unauthorized access, or performing actions that compromise security. Instead of exploiting software vulnerabilities, social engineering exploits cognitive biases trust, authority, fear, and the tendency to comply with perceived superiors.

In a social engineering attack, the perpetrator manipulates human psychology rather than technical systems to gain unauthorized access to sensitive data or network resources. Attackers often present themselves as trustworthy figures, such as a new employee, maintenance worker, or researcher, and may fabricate credentials to reinforce their false identity. Through seemingly routine conversations, they gradually extract enough details to compromise an organization's security. If one individual does not provide sufficient information, the attacker can approach another employee within the same organization, using the initial data to appear more credible and increase the likelihood of success (CISA,2021). Social engineering was employed in 98% of cyberattacks in 2022, demonstrating just how widely adopted this form of psychological manipulation has become among threat actors (Sayler, 2023).
## Phishing attacks
Phishing is a social engineering technique in which attackers send fraudulent emails or direct victims to malicious websites that mimic legitimate organizations. By posing as a trusted entity—such as a bank, credit card company, or government agency—attackers request sensitive information, often under the pretense of an urgent issue requiring immediate action. Victims who comply unknowingly hand over their credentials or personal data, which attackers then use to compromise their accounts (CISA, 2021).
*Types of phishing attack*:
 - Vishing attack: Vishing is a social engineering attack conducted over voice communication, such as phone calls. Attackers may trick victims into calling a fraudulent number to disclose sensitive information. More advanced vishing attacks use Voice over Internet Protocol (VoIP) services, which allow attackers to easily spoof caller ID, making a call appear to come from a trusted source. Many people mistakenly trust phone calls, especially landlines, because they believe these lines are secure. However, while landlines cannot be intercepted without physical access, this does not protect against speaking directly to a scammer (CISA, 2021).
 - Smishing attack: Smishing is a social engineering attack that uses SMS (text) messages to deceive victims. These messages often contain links to malicious websites, email addresses, or phone numbers. When clicked, these links can automatically open a browser, launch an email, or dial a number. The seamless integration between text messaging, email, voice calls, and web browsing increases the chances that users will be tricked into falling for the attack (CISA, 2021).

 - Spear phishing: Spear phishing is a targeted form of phishing that focuses on specific employees or departments within an organization. Rather than exclusively targeting C-suite executives, attackers often aim for HR personnel, IT administrators, finance teams, and other staff members who have access to valuable systems, data, or business processes.These attacks typically involve highly customized emails or messages that appear to come from a trusted vendor, internal colleague, or service provider. The objective is to deceive just one individual into clicking a malicious link, downloading an infected attachment, approving a fraudulent request, or submitting sensitive information (Danielson, 2026).
 - Whaling: Whaling is a specialized form of phishing that targets senior executives and key decision-makers within an organization, such as the CEO, CFO, and other C-suite members. These individuals are prime targets because they possess access to sensitive financial systems and have the authority to approve substantial transactions.Attackers exploit the typical behavior of executives, who often work irregular hours, make urgent decisions, and follow distinct communication patterns. By studying these habits, cybercriminals craft convincing scams tailored to their targets (Danielson, 2026).
## Real world case study
### Google Sues to Disrupt Chinese SMS Phishing Triad
According to Krebs(2025), In November 2025, Google filed a lawsuit in the Southern District of New York against 25 unnamed individuals connected to "Lighthouse," a sophisticated phishing-as-a-service (PhaaS) operation based in China. The service enabled cybercriminals to mass-send fraudulent SMS messages impersonating trusted brands including the U.S. Postal Service, toll road operators, e-commerce websites, financial institutions, and brokerage firms to steal payment card data from mobile users across 120 countries, harming over one million victims.
Victims received a spoofed text message claiming an urgent issue (e.g., delivery fee or delinquent toll). Clicking the link led to a phishing website mimicking a trusted brand. After victims entered their card details, the site attempted to enroll the card in a mobile wallet (Apple Pay or Google Pay). Victims were then prompted to enter a one-time verification code sent by their bank. Once provided, attackers linked the card to a device they controlled, enabling fraudulent purchases.

 - Over 600 phishing templates for more than 400 entities
 - Google's logos appeared on at least 25% of templates· 300+ front desk staff supporting fraud operations
 - Approximately 25,000 phishing domains active during any 8-day period.
 
Additional Tactic: Lighthouse also enabled fake e-commerce sites advertised via Google Ads (paid with stolen cards). Victims never received purchases, while attackers enrolled cards in mobile wallets and made fraudulent charges. While Google's legal action may temporarily disrupt operations, experts warn the group will likely rebrand or redevelop given the lucrative mobile phishing market.
### How to Avoid Being a Victim:

 - Be suspicious of unsolicited calls, visits, or emails asking for internal information.
 - Verify the identity of anyone claiming to be from a legitimate organization by contacting the company directly use contact information from official statements, not from the request itself.
 - Never provide personal, financial, or organizational information unless you are certain of the person's authority.
 - Do not respond to email requests for personal or financial information or click links in such emails.
 - Before sending sensitive information online, check for "https" and a closed padlock icon in the browser
 - Stay informed about known phishing attacks through resources like the Anti-Phishing Working Group (CISA, 2021).
## Pretexting
Pretexting is a social engineering technique where an attacker creates a fake identity, role, or scenario to manipulate a target into doing something they normally wouldn't do. The fabricated story known as the "pretext" makes the request appear legitimate to the victim. Nearly every social engineering attack, whether phishing, business email compromise, or helpdesk fraud, depends on a pretext to gain trust and bypass suspicion. The quality of a pretext depends directly on the quality of reconnaissance. Attackers gather employee names, job titles, reporting structures, internal tools, vendors, project timelines, and upcoming events to craft believable scenarios. AI tools now automate this process by scanning the web for company information and building detailed employee profiles that make attacks more convincing. Voice cloning requires only a short audio sample, making any executive with public speaking appearances a viable impersonation target (Evers, 2026).
### Real-world case study

#### Why You Should Opt Out of Sharing Data With Your Mobile Provider

In March 2023, AT&T disclosed a data breach involving a marketing vendor that exposed Customer Proprietary Network Information (CPNI) for approximately 9 million customers. The exposed data included customer names, wireless account numbers, phone numbers, email addresses, and in some cases, rate plan names, past due amounts, monthly payments, and minutes used (Krebs, 2023).
CPNI is valuable to attackers because it provides detailed metadata about a customer's telecommunications usage such as called numbers, call times, call lengths, billing details, and service features. While CPNI is considered private and cannot be used directly for marketing, carriers share it with partner companies for network operating reasons. Additionally, mobile internet usage (websites visited, search history, apps used) is not protected under CPNI rules because carriers act as information services providers, allowing them to share and sell this data (Krebs, 2023).
Attackers can use exposed CPNI data to build convincing pretexts. For example: 

 - Impersonating a telecom representative to request account changes 
 - Posing as a financial institution with knowledge of recent transactions
 - Using call records and billing details to validate a false identity when calling a helpdesk Researchers have demonstrated that supposedly "anonymized" browsing data can be de-anonymized, making it easier for attackers to profile targets (Krebs, 2023).
 
 While AT&T stated the breach did not expose sensitive information like credit card numbers or passwords, the exposed CPNI provides attackers with a wealth of personal metadata enough to craft highly believable pretexts that bypass typical suspicion.
 
### Pretexting preventions
 - Map Your Vulnerabilities::Identify which roles in your organization are most at risk (e.g., helpdesk, finance, HR, vendors) and document the types of pretexts attackers commonly use against them.
 - Monitor for Attack Infrastructure: Continuously watch for suspicious domains, fake social media profiles, spoofed phone numbers, and fraudulent apps these are early warning signs of an impending pretexting campaign.
 - Remove Attacker Assets at the Source: Work with registrars, hosting providers, social platforms, and telecoms to take down attacker infrastructure quickly. The faster they lose their tools, the less profitable their operation becomes.
 - Train Employees with Realistic Scenarios: Replace generic training with role-specific simulations based on actual attacks seen in your industry. Finance teams should practice against executive impersonation attempts; helpdesk staff should train against fraudulent password reset requests. Repetition builds instinct (Evers, 2026).
### Baiting
Baiting is a social engineering attack that lures victims into revealing sensitive information or installing malware by offering something appealing, such as a fake website mimicking a trusted service, an email from a familiar source, or promises of rewards like contest winnings or free downloads. Attackers exploit human curiosity, greed, and urgency to manipulate victims into clicking malicious links or downloading infected files. Modern attackers increasingly use artificial intelligence to generate polished, highly targeted messages in seconds and in multiple languages, making these lures significantly harder to detect (Bitwarden, n.d.).
### Types of Baiting Attacks
Baiting attacks take several forms, each exploiting different vulnerabilities and delivery channels:
 - Physical baiting: One of the oldest methods, involving tangible items like infected USB drives or external hard drives deliberately left in public places such as parking lots or lobbies. When an unsuspecting individual plugs the device into their computer, malware installs silently, giving attackers access to sensitive systems or files (Bitwarden, n.d.).
 - Digital baiting: Conducted online through fake giveaways, free software offers, or malicious links. These attacks are designed to trick users into downloading malware or entering personal information. Digital baiting can reach large audiences and is frequently disguised as a legitimate offer, such as a trusted service or familiar brand (Bitwarden, n.d.).
### Real-world case study 
Google Docs “Invitation” attack (2017): Attackers sent millions of users what appeared to be a legitimate Google Docs share invitation. Clicking the link led to a malicious app authorization request that, if approved, gave attackers access to the victim’s Google account and contact list. The lure was a familiar, trusted service, making it a clear case of digital baiting(Bitwarden, n.d.).
### Prevention measures for Baiting
 - Establish clear policies for device handling, external media usage, and BYOD practices to minimize physical and digital attack surfaces.
 - Enable Multi-Factor Authentication (MFA) to add an additional verification step for all logins.
 - Use anti-phishing and anti-malware tools to scan emails, attachments, and downloads, neutralizing threats before they execute (Bitwarden, n.d.).
### Quid Pro Quo
A quid pro quo attack is a social engineering tactic where an attacker offers a service, gift, or benefit in exchange for sensitive information or system access from the victim. A quid pro quo attack exploits the principle of reciprocity attackers promise help, a gift, or a service in exchange for cooperation. A common tactic involves an impostor posing as IT support, calling employees and offering to fix a non-existent issue if the victim provides their credentials, disables antivirus software, or installs a "diagnostic" tool that is actually malware. Other variations include fake survey rewards, free software, or premium content offered in exchange for login details(Cyber Glossary, n.d.).
### Preventions measures for quid pro quo 
 - Verifying support requests through official channels 
 - Restricting administrative actions to trusted helpdesk identities
 - Providing security awareness training
 - Offering employees an easy way to validate unsolicited contacts (Cyber Glossary, n.d.).


## Social Engineering Attacks Comparison Table

| Attack Type | Primary Target | Psychological Lever Exploited | Best Countermeasure |
|-------------|---------------|------------------------------|---------------------|
| **Phishing** | General employees (mass emails) | Fear, urgency, authority | Email filtering + anti-phishing tools |
| **Spear Phishing** | Specific individuals (HR, finance, IT) | Trust, personalization | Role-based training + email verification |
| **Whaling** | C-suite executives (CEO, CFO) | Authority, urgency | Executive-specific training + transaction verification |
| **Vishing** | Employees via phone calls | Trust in caller ID, authority | Caller verification + avoid sharing sensitive info over phone |
| **Smishing** | Mobile users via SMS | Urgency, curiosity | Link verification + mobile security awareness |
| **Pretexting** | Employees with access to sensitive data | Trust in fabricated identity | Independent verification + reconnaissance monitoring |
| **Baiting (Physical)** | Employees in public spaces | Curiosity, greed | Strict USB/media policies + security awareness |
| **Baiting (Digital)** | Internet users (fake offers, downloads) | Greed, fear, urgency | Anti-malware tools + link verification |
| **Quid Pro Quo** | Employees receiving unsolicited calls | Reciprocity, desire for help | Identity verification + ticketing systems |

### Organizational recommendations 
1. Recognize Social Engineering Tactics: Train employees to identify common techniques including phishing, pretexting, baiting, vishing, smishing, and quid pro quo. Teach them to spot red flags such as unsolicited requests, urgent language, grammatical errors, suspicious sender addresses, and offers that seem too good to be true.
2. Verify Before Trusting: Encourage a culture of independent verification. Employees should always confirm the identity of anyone requesting sensitive information or system access through official, verified channels not through contact details provided in the request itself.
3. Handle External Media and Devices with Caution: Establish strict policies for USB drives, external hard drives, and other removable media. Employees should never connect unknown devices to company systems and should report suspicious physical items found on premises.
4. Practice Strong Password and MFA: Require strong, unique passwords (at least 16 characters with a mix of uppercase, lowercase, numbers, and symbols) for all accounts and enforce Multi-Factor Authentication wherever possible. Encourage the use of password managers.
5. Report Suspicious Activity Immediately: Create a clear, non-punitive reporting process for employees to report potential social engineering attempts. Quick reporting enables faster incident response and helps protect the entire organization.

## References
1. Cybersecurity and Infrastructure Security Agency (CISA). (2021, February 1). Avoiding Social Engineering and Phishing Attacks. https://www.cisa.gov/news-events/news/avoiding-social-engineering-and-phishing-attacks 
2. Danielson, L. (2026, June 18). Whaling vs. Spear Phishing: How Cybercriminals Target Executives and Organizations? https://www.huntress.com/phishing-guide/spear-phishing-vs-whaling
3. Krebs, B. (2025, November 13). Google Sues to Disrupt Chinese SMS Phishing Triad. Krebs on Security. https://krebsonsecurity.com/2025/11/google-sues-to-disrupt-chinese-sms-phishing-triad/
4. Evers, J. (2026, May 22). Pretexting Attacks: How Social Engineering Attacks Build Trust Before They Strike. Security Boulevard. https://securityboulevard.com/2026/05/pretexting-attacks-how-social-engineering-attacks-build-trust-before-they-strike/
5. Bitwarden.(n.d.). Baiting attacks explained: How to recognize and prevent them [Resource Center].https://bitwarden.com/resources/baiting-attacks-explained/#real-world-examples-of-baiting-attacks
6. Cyber Glossary. (n.d.). Quid Pro Quo Attack (Entry #1000). Reviewed by Florian Amette.https://www.cyberglossary.org/en/term/quid-pro-quo-attack
