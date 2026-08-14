# Patch Management 
Definition:
Patch Management is the act of applying a change to installed software such as firmware, operating systems, or applications that corrects security or functionality problems or adds new capabilities (Souppaya & Scarfone, 2022, p. 6).
#### Role within the vulnerability lifecycle:
Within the software vulnerability management life cycle, patch management functions as the primary means of taking action against security flaws. This life cycle encompasses identifying vulnerabilities, determining how to address them, and carrying out that response through preparation, deployment, verification, and ongoing oversight (Souppaya & Scarfone, 2022, pp. 11–12). What sets patching apart from other risk responses is that it "is the only form of risk response that can completely eliminate the vulnerabilities without removing functionality" (Souppaya & Scarfone, 2022, p. 10). NIST further stresses that "preventive maintenance through enterprise patch management helps prevent compromises, data breaches, operational disruptions, and other adverse events" (Souppaya & Scarfone, 2022, p. 4). In essence, patch management powers the vulnerability lifecycle it is the practical method organizations rely on to remediate flaws, from initial awareness through to sustained monitoring. Without it, the vulnerability lifecycle lacks an effective mechanism for action, leaving organizations vulnerable to serious cybersecurity threats.
#### Why patches matter?
Organizations must stay informed about new software vulnerabilities that impact their systems, including applications, operating systems, and firmware. This requires maintaining a detailed inventory of all assets and the specific software versions they run, down to individual packages and libraries, while actively monitoring for new vulnerabilities affecting those components. To achieve this, organizations can subscribe to vulnerability feeds from software vendors, security researchers, and the National Vulnerability Database (NVD) (Souppaya & Scarfone, 2022, p. 11).
Applying patches sooner shortens the time attackers have to exploit vulnerabilities, but it also raises the likelihood of operational issues due to insufficient testing. Computing technologies require ongoing maintenance because there are countless individuals worldwide who constantly seek out and take advantage of software flaws (Souppaya & Scarfone, 2022, pp. 6, 15).
### Real-world case studies
#### What You Should Know About the Equifax Data Breach Settlement
In 2017, Equifax ,one of the three major U.S. credit bureaus suffered a massive data breach that exposed the personal and financial information of approximately 148 million Americans. The breach was caused by Equifax's failure to patch a known vulnerability in Apache Struts (CVE-2017-5638). Although a patch was available, Equifax did
not apply it in a timely manner, allowing attackers to exploit the flaw months later (Krebs, 2019).
#### No Jail Time for “WannaCry Hero”
In May 2017, the WannaCry ransomware spread rapidly across the globe, infecting over 200,000 computers across 150 countries and causing billions in damages. WannaCry exploited a vulnerability in Microsoft's Server Message Block version 1 (SMBv1) protocol, known as EternalBlue (CVE-2017-0144). The vulnerability was originally developed by the U.S. National Security Agency (NSA) and later stolen and leaked by a hacking group called the Shadow Brokers.Microsoft had released a patch (MS17-010) two months prior to the outbreak in March 2017 . However, many organizations failed to apply it, leaving themselves vulnerable to the rapidly spreading ransomware(Krebs,2019).
### consequences of not patching 
The NIST establishes that failing to patch leads to data breaches, ransomware attacks, operational disruptions, reputational damage, and potential legal and financial consequences (Souppaya & Scarfone, 2022). The Equifax breach demonstrates these consequences on a massive scale, exposing 148 million records and costing over $650 million (Krebs, 2019). Meanwhile, WannaCry exploited organizations that had not applied a patch released two months earlier, infecting over 200,000 systems globally (Krebs, 2019). Timely patching is critical to preventing major cybersecurity incidents. 
### Patch Management Lifecycle

 - Discovery: Organizations must identify their assets and the software versions running on them, down to individual packages and libraries.Vulnerability feeds from software vendors, security researchers, and the National Vulnerability Database (NVD) should be monitored to stay informed of new vulnerabilities.
 - Assessment: Once a vulnerability is identified, organizations assess the risk it poses to determine the appropriate response.Organizations choose how to respond whether to accept, mitigate (patch), transfer, or avoid the risk.
 - Testing: Before deployment, patches should be tested to identify potential problems and reduce operational risk.Testing can be performed manually or through automated methods.
 - Deployment: Patches are distributed and installed on affected assets.Deployment methods vary based on the type of software (firmware, operating system, application), asset platform (IT, OT, IoT, mobile, cloud), and environmental limitations.Some installations require administrator privileges or user participation.
 - Verification: Organizations confirm that patches have been installed successfully and have taken effect.Automated means are generally needed to achieve verification at scale.
 - Continuous Monitoring (Additional Phase): Organizations monitor deployed patches to ensure they remain installed and have not been removed by users, attackers, or system resets. Monitoring also helps detect any changes in patched software behavior that might indicate issues (Souppaya & Scarfone, 2022).
### Prioritised 7-Steps of Patch Management
 - Inventory All Assets and Software: maintain a current inventory of all physical and virtual computing assets. Track software versions down to individual packages and libraries. Use automation to continuously discover new assets and collect information. Include each asset's technical and mission/business characteristics.
 - Define Risk Response Scenarios: Prepare for routine patching (standard patches). Plan for emergency patching (severe or actively exploited vulnerabilities). Establish emergency mitigation procedures (temporary fixes when patches are unavailable). Address unpatchable assets through isolation and alternative protections.
 -  Assign Assets to Maintenance Groups: Group assets with similar characteristics and maintenance needs. Define groups at the appropriate level of detail. Periodically review and adjust group definitions.
 - Create Maintenance Plans for Each Group: Specify actions, timeframes, and rollback procedures for each scenario. Use phased deployments with small test groups ("canaries") before full rollout. Set deadlines for patch installation with enforcement mechanisms. Track and monitor all exceptions closely.
 - Minimise Patching Disruptions: Harden software by removing unnecessary features and enforcing least privilege. Choose platforms where patching is less disruptive (e.g., cloud containers). Use managed services instead of self-managed software where practical.
 - Track Meaningful Metrics: Measure patch performance by asset and vulnerability importance. Track percentage of assets patched by deadlines. Measure average and median time to patch. Analyse data by platform, business unit, and maintenance group to identify improvement areas.
 - Evaluate Vendor Patch Practices in Procurement. Assess vendor patching practices before purchasing software. Inquire about update frequency, testing procedures, and typical disruption levels. Evaluate vendor transparency in security communications (Souppaya & Scarfone, 2022).
### Challenges
#### Challenge 1
Legacy Systems:
Why it's a challenge: Legacy systems may no longer be supported by vendors, meaning patches are never released. Older software often cannot be patched without breaking critical functionality, and some assets must run uninterrupted for extended periods because they provide mission-critical functions. 

How to overcome: 
 - Isolate unpatched legacy assets using network segmentation and micro-segmentation.
 - Implement additional security controls to reduce the attack surface
 - Plan for periodic reevaluation of alternatives to patching (Souppaya & Scarfone, 2022).
  
  #### Challenge 2: 
  
 Downtime Concerns
 Why it's a challenge:Business and mission owners often resist patching because they fear operational disruption and downtime. Many view patching as harmful to productivity rather than essential maintenance (Souppaya & Scarfone, 2022).
 
 How to overcome:
 
 - Frame patching as preventive maintenance disruptions from patching are controllable, while disruptions from incidents are largely uncontrollable.
 - Schedule maintenance windows and communicate them across the organization
 - Use phased deployments to test impact before full rollout (Souppaya & Scarfone, 2022)

#### Challenge 3: 

Testing Requirements
Why it's a challenge: Testing takes time and resources. Organizations must balance the need for rapid deployment against the risk of operational issues. Deploying patches more quickly reduces the attacker's window of opportunity but increases the risk of disruption from insufficient testing(Souppaya & Scarfone, 2022).

How to overcome:
 - Use phased deployments with "canary" assets a small subset receives patches first to identify issues before wider rollout.
 - Start with technically knowledgeable users, then expand to early adopters.
 - For critical security patches, use accelerated schedules with limited testing windows.

## References

 1. Krebs, B. (2019, July 22). What you should know about the Equifax data breach settlement. KrebsOnSecurity. https://krebsonsecurity.com/2019/07/what-you-should-know-about-the-equifax-data-breach-settlement/  
 2. Souppaya, M., & Scarfone, K. (2022). Guide to enterprise patch management planning: Preventive maintenance for technology (NIST Special Publication 800-40 Revision 4). National Institute of Standards and Technology. 
 3. Krebs, B. (2019, July 29). No jail time for "WannaCry hero." KrebsOnSecurity. https://krebsonsecurity.com/2019/07/no-jail-time-for-wannacry-hero/
 
