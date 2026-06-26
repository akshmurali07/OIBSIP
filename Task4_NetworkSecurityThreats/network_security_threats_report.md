# Title: Research Report on Common Network Security Threats
# Prepared by: Akshara Murali
# Internship: AICTE Oasis Infobyte - Security Analyst Internship
# Task 4: Research Report on Common Network Security Threats
# Date: June 2026

## 1.Introduction
In today's digitally connected world, network security has become a critical concern for organizations of all sizes. As businesses increasingly rely on networked systems to store and transmit sensitive data, the threat landscape continues to evolve. This report provides a comprehensive overview of the most common network security threats, how they work, their real-world impact, and the mitigation strategies available to defend against them.

## 2. Denial of Service (DoS) and Distributed Denial of Service (DDoS) Attacks
- 2.1 How It Works
- A Denial of Service attack floods a target system, server, or network with excessive traffic or requests, overwhelming it to the point where it becomes unavailable to legitimate users. A Distributed DoS (DDoS) attack scales this up by using thousands of compromised machines (called a botnet) to launch the attack simultaneously.
- 2.2 Impact
- •	Website and service downtime leading to financial loss
- •	Damage to brand reputation and customer trust
- •	Disruption of critical infrastructure such as hospitals, banks, and government services
- 2.3 Real-World Example
- In 2016, the Mirai botnet launched a massive DDoS attack on Dyn, a DNS provider, taking down major websites including Twitter, Netflix, Reddit, and GitHub for several hours.
- 2.4 Mitigation Strategies
- •	Use rate limiting and traffic filtering on firewalls
- •	Deploy Content Delivery Networks (CDNs) to distribute traffic load
- •	Use DDoS protection services such as Cloudflare or AWS Shield
- •	Monitor network traffic in real time for anomaly detection
- •	Implement IP blacklisting for known malicious sources

## 3. Man-in-the-Middle (MITM) Attacks
- 3.1 How It Works
- In a Man-in-the-Middle attack, an attacker secretly intercepts and possibly alters the communication between two parties who believe they are communicating directly with each other. This is typically done through techniques such as ARP spoofing, SSL stripping, or rogue Wi-Fi hotspots.
- 3.2 Impact
- •	Theft of sensitive data including login credentials, financial details, and personal information
- •	Session hijacking allowing attackers to impersonate legitimate users
- •	Unauthorized data modification during transmission
- 3.3 Real-World Example
- In 2011, DigiNotar, a Dutch certificate authority, was compromised, allowing attackers to issue fraudulent SSL certificates and perform MITM attacks on Iranian Gmail users, intercepting their private communications.
- 3.4 Mitigation Strategies
- •	Always use HTTPS and enforce SSL/TLS encryption
- •	Implement certificate pinning in applications
- •	Use VPNs especially on public Wi-Fi networks
- •	Enable multi-factor authentication (MFA) to reduce impact of credential theft
- •	Deploy Intrusion Detection Systems (IDS) to identify suspicious traffic

## 4. IP Spoofing
- 4.1 How It Works
- IP spoofing involves an attacker forging the source IP address in network packets to disguise their identity or impersonate another system. This is commonly used to bypass IP-based authentication, launch DDoS attacks, or redirect traffic.
- 4.2 Impact
- •	Bypass of access controls and authentication systems
- •	Used as a component in larger attacks like DDoS amplification
- •	Can lead to misdirection of network traffic and data interception
- 4.3 Real-World Example
- IP spoofing was a key technique used in the 2018 Memcached DDoS amplification attacks, where attackers sent spoofed requests to Memcached servers, which then flooded victims with amplified responses - one of the largest DDoS attacks ever recorded, peaking at 1.7 Tbps.
- 4.4 Mitigation Strategies
- •	Use ingress and egress filtering on routers (BCP38 standard)
- •	Implement network authentication protocols such as IPsec
- •	Configure firewalls to reject packets with internal source addresses arriving from external interfaces
- •	Use encrypted protocols to validate packet origins

## 5. DNS Spoofing (DNS Cache Poisoning)
- 5.1 How It Works
- DNS spoofing involves corrupting the DNS cache of a resolver so that it returns a fraudulent IP address for a domain name. This redirects users to malicious websites without their knowledge.
- 5.2 Impact
- •	Users are silently redirected to phishing or malware-hosting websites
- •	Credential theft and malware infection
- •	Disruption of internet services at scale
- 5.3 Real-World Example
- In 2010, users in Brazil were victims of a large-scale DNS cache poisoning attack targeting a major ISP, redirecting customers to malicious pages that installed banking trojans on their systems.
- 5.4 Mitigation Strategies
- •	Enable DNSSEC (DNS Security Extensions) to cryptographically sign DNS records
- •	Regularly flush and monitor DNS caches
- •	Use trusted and up-to-date DNS resolvers
- •	Monitor for unexpected DNS record changes

## 6. Packet Sniffing
- 6.1 How It Works
- Packet sniffing involves capturing data packets as they travel across a network using tools like Wireshark. While used legitimately by network administrators, attackers can use it to steal unencrypted data.
- 6.2 Impact
- •	Exposure of plaintext credentials, emails, and sensitive files
- •	Session token theft enabling account takeover
- •	Corporate espionage through traffic analysis
- 6.3 Real-World Example
- In many public Wi-Fi environments, unencrypted HTTP traffic has been captured by attackers using freely available sniffing tools, leading to widespread credential theft.
- 6.4 Mitigation Strategies
- •	Enforce end-to-end encryption using TLS/SSL for all communications
- •	Use switched networks instead of hub-based networks
- •	Deploy network monitoring tools to detect unauthorized sniffers
- •	Educate users to avoid transmitting sensitive data over unsecured networks

## 7. Conclusion
- Network security threats are constantly evolving and pose significant risks to individuals, businesses, and critical infrastructure. Understanding how attacks such as DoS/DDoS, Man-in-the-Middle, IP Spoofing, DNS Spoofing, and Packet Sniffing work is the first step towards building effective defenses. Organizations must adopt a layered security approach combining encryption, monitoring, access controls, and user education to stay protected against these threats.

### 8. References
•	Stallings, W. (2017). Network Security Essentials: Applications and Standards. Pearson.
•	OWASP Foundation. (2023). Network Security Threats Overview. https://owasp.org
•	CISA. (2023). Understanding Denial-of-Service Attacks. https://www.cisa.gov
•	Cloudflare. (2023). What is a DDoS Attack? https://www.cloudflare.com/learning/ddos
•	NIST. (2023). Guidelines on Firewalls and Firewall Policy. https://csrc.nist.gov
