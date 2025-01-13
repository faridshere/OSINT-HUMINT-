# OSINT-HUMINT

Investigating a Simulated Phishing Campaign Using OSINT and HUMINT Techniques

1. Overview
This project investigates the domain oersonalcapital.com, suspected of impersonating personalcapital.com AND EMPOWER.COM, using OSINT (Open Source Intelligence) and simulated HUMINT (Human Intelligence) techniques. The goal is to gather and analyze indicators of compromise (IOCs), identify attacker tactics, techniques, and procedures (TTPs), and propose actionable mitigation strategies.

2. Objectives
- Collect threat intelligence using OSINT tools.
- Identify key IOCs (e.g., phishing domains, IPs, emails).
- Analyze attacker TTPs through simulated HUMINT.
- Provide actionable recommendations to mitigate the phishing campaign.

3. Tools Used  
- **OSINT Framework**: List of OSINT tools.
- **Maltego CE**: Relationship mapping.
- **VirusTotal**: Domain, file, and URL scanning.
- **Hunter.io**: Discover email addresses linked to the domain.
- **Have I Been Pwned**: Check breached emails.
- **Shodan**: Search for internet-connected devices.
- **ThreatMiner**: Domain reputation analysis.
- **Google Dorking**: Advanced search queries.

4. Workflow 
**4.1. Initial Analysis**  
- **Domain**: oersonalcapital.com  
- **Registrar**: Cosmotown, Inc.  
- **Creation Date**: December 25, 2024  
- **DNSSEC**: Not signed  
- **Nameservers**: Benedict.NS.Cloudflare.com, Sofia.NS.Cloudflare.com  
- **Hosting Provider**: Google Cloud Platform  
- **Indicators of Malicious Behavior**: Newly registered domain, typo-squatting, and use of Cloudflare to obscure true hosting.
- IP Analysis
Investigate IPs contacted:
Main IP: 104.82.85.154 (Akamai, Hamburg, Germany).

**4.2. OSINT Analysis**  
- **Domain Reputation**: Use WHOIS and ThreatMiner to assess the domain's history and reputation.  
- **URL & File Scanning**: Analyze URLs and files linked to the domain via VirusTotal.  
- **Email & Breach Check**: Identify associated emails with Hunter.io and check breaches via Have I Been Pwned.  
- **Infrastructure Trace**: Use Shodan for hosting and IP details, and map relationships with Maltego CE.

**4.3. Simulated HUMINT**  
- **Attacker Intent**: Likely phishing for credentials or financial theft via urgency-based emails.  
- **TTPs**: Typo-squatting domain, exploiting Cloudflare for infrastructure obfuscation.

**5. Findings**  
**5.1. IOCs**  
- **Domain**: oersonalcapital.com  
- **IP Address**: Associated with Google Cloud Platform (104.82.85.154).  
- **Email Addresses**: Detected emails like support@oersonalcapital.com via Hunter.io.  
- **URLs**: Links to fake login pages.

**5.2. Attacker Profile**  
- Likely financially motivated with tactics like typo-squatting and urgency-based phishing.  
- Potential links to organized campaigns targeting financial institutions.

**6. Recommendations**  
**6.1. Immediate Actions**  
- **Block IOCs**: Add oersonalcapital.com to blocklists and restrict access to associated IPs.  
- **Report to Providers**: Notify Cloudflare and Google Cloud Platform.  
- **Educate Users**: Train staff to recognize phishing and typo-squatting.

**6.2. Preventive Measures**  
- **Email Security**: Implement DMARC, DKIM, and SPF protocols.  
- **Regular Monitoring**: Continuously scan for similar domains and use automated threat intelligence tools.

