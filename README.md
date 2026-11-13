# CYBERSECURITY TECHNICAL REPORT
## WEEK 02 – FOOTPRINTING, OSINT & NETWORK DISCOVERY

**NETWORKWALKS CYBERSECURITY INTERNSHIP PROGRAM**

| **Report information** | **Details** |
|---|---|
| Student Name | ROSY NDONGO EKOUM |
| Program / Batch | B084 |
| Internship Week | Week 02 |
| Report Date | 13 November 2026 |
| Organization | Networkwalks |
| Operating System | Kali Linux |
| Modules covered | W2-PM1, W2-PM3, W2-PM4, W2-PM5 |
| Main tools | Kali Linux, Maltego, theHarvester, Zenmap |

---

# 1. DISCLAIMER AND SCOPE OF WORK

All activities described in this report were performed for educational and cybersecurity training purposes as part of the Networkwalks Cybersecurity Internship Program.

The practical exercises focused on information gathering, Open-Source Intelligence (OSINT), footprinting and network discovery.

Activities involving Networkwalks were limited to the scope authorized by the internship instructions. The Microsoft domain exercise is documented as a passive OSINT information-gathering exercise. No exploitation, authentication attempts, vulnerability testing or active scanning of Microsoft infrastructure was performed.

The results presented in this report represent observations obtained during the exercises. They should not be interpreted as confirmation of active vulnerabilities, accessible systems or compromised accounts.

All cybersecurity activities must be conducted within an explicitly authorized scope and in accordance with applicable laws and ethical principles.

# 2. INTRODUCTION

During Week 02 of the Networkwalks Cybersecurity Internship Program, I worked on practical exercises related to reconnaissance, footprinting, Open-Source Intelligence (OSINT) and network discovery.

The main objective was to understand how publicly available information can be collected and analyzed to build an initial picture of a target's digital presence.

Several tools were used to explore different aspects of reconnaissance. Maltego was used to identify relationships between publicly available information associated with the Networkwalks domain. TheHarvester was used to collect publicly indexed information, including email addresses, IP addresses, hostnames and other domain-related data.

Additional exercises involved Kali Linux footprinting tools and Zenmap for network discovery in a controlled environment.

This report describes the methodology followed, the tools used, the observations obtained, their potential security implications and the limitations encountered during the exercises.

# 3. OBJECTIVES

The main objectives of this week's practical activities were:

1. Understand the reconnaissance and footprinting phases of a cybersecurity assessment.
2. Learn how to collect publicly available information about a domain.
3. Identify relationships between information using Maltego.
4. Use theHarvester to discover publicly indexed email addresses, hostnames and other domain-related information.
5. Understand the role of different Kali Linux reconnaissance tools.
6. Practice network discovery using Zenmap in an authorized environment.
7. Interpret findings and understand their potential security implications.
8. Document technical activities and observations in a structured report.

# 4. TOOLS AND TECHNOLOGIES USED

The following tools were used or considered during the practical exercises.

| Tool | Purpose |
|---|---|
| Kali Linux | Linux distribution used for cybersecurity and reconnaissance activities. |
| WHOIS | Retrieves publicly available domain registration information. |
| WhatWeb | Identifies technologies used by a website. |
| Nslookup | Resolves domain names and retrieves DNS information. |
| cURL | Retrieves HTTP response information and headers. |
| Wafw00f | Identifies possible Web Application Firewall technologies. |
| DNSRecon | Collects and analyzes DNS-related information. |
| Maltego | Visualizes relationships between entities and publicly available information. |
| theHarvester | Collects publicly available emails, hosts, IP addresses and other domain-related information. |
| Zenmap | Graphical interface for Nmap, used for network discovery and scanning. |

# 5. ACTIVITIES PERFORMED

## 5.1. Footprinting and Reconnaissance with Kali Linux – W2-PM1

The first practical activity focused on footprinting and reconnaissance using Kali Linux tools.

Footprinting is the process of collecting information about a target before conducting further security assessments. This information can include domain registration details, DNS records, web technologies, server information and other publicly accessible data.

The following tools were included in the practical exercise.

### 5.1.1. WHOIS

WHOIS is used to retrieve publicly available information about a domain name, including registration details, registrar information, registration dates and name servers.

**Command used:**

`whois [target-domain]`

**Observation:**

[Insert the actual WHOIS results obtained during your exercise.]

**Security relevance:**

Domain registration information can help security professionals understand the ownership and infrastructure associated with a domain. It can also provide information that may be useful during reconnaissance.

**Evidence:** [Insert Screenshot 1 – WHOIS results]

### 5.1.2. WhatWeb

WhatWeb is a web technology fingerprinting tool. It helps identify technologies and services used by a website, such as content management systems, frameworks and web server technologies.

**Command used:**

`whatweb [target-domain]`

**Observation:**

[Insert the technologies and other relevant information identified by WhatWeb.]

**Security relevance:**

Identifying web technologies helps security professionals understand the target's technology stack and determine whether further authorized security reviews are necessary.

**Evidence:** [Insert Screenshot 2 – WhatWeb results]

### 5.1.3. Nslookup

Nslookup is a command-line utility used to query DNS servers and retrieve information about domain names.

**Command used:**

`nslookup [target-domain]`

**Observation:**

[Insert the IP address and other DNS information returned by your command.]

**Security relevance:**

DNS information helps identify how a domain resolves on the Internet and provides an initial understanding of its network infrastructure.

**Evidence:** [Insert Screenshot 3 – Nslookup results]

### 5.1.4. cURL – HTTP Headers

cURL can be used to retrieve HTTP response headers from a website.

**Command used:**

`curl -I https://[target-domain]`

**Observation:**

[Insert the HTTP status code and relevant response headers returned by your command.]

**Security relevance:**

HTTP headers can reveal information about the web server and application configuration. Reviewing them can help identify unnecessary technical information exposed to external users.

**Evidence:** [Insert Screenshot 4 – cURL results]

### 5.1.5. Wafw00f

Wafw00f is a tool designed to identify whether a website is protected by a Web Application Firewall (WAF) and, when possible, identify the technology used.

**Command used:**

`wafw00f https://[target-domain]`

**Observation:**

[Insert the actual result: WAF detected, no WAF detected, or inconclusive.]

**Security relevance:**

Knowing whether a WAF is present provides information about the website's defensive architecture. However, identifying a WAF does not establish whether it is correctly configured or effective against every attack.

**Evidence:** [Insert Screenshot 5 – Wafw00f results]

### 5.1.6. DNSRecon

DNSRecon is a DNS enumeration tool used to retrieve and analyze DNS records.

**Command used:**

`dnsrecon -d [target-domain]`

**Observation:**

[Insert the DNS records or other relevant findings obtained.]

**Security relevance:**

DNS records can reveal information about name servers, mail infrastructure and other services associated with a domain. This information can help build a broader understanding of the target's digital infrastructure.

**Evidence:** [Insert Screenshot 6 – DNSRecon results]

---

## 5.2. Relationship Discovery with Maltego – W2-PM3

### 5.2.1. Overview

Maltego is an OSINT and link-analysis platform used to visualize relationships between different entities.

It allows investigators to explore connections between information such as domains, email addresses, organizations, websites and other publicly available data.

The objective of this practical exercise was to explore information associated with the Networkwalks domain and identify relationships using Maltego.

### 5.2.2. Methodology

The exercise was performed using Maltego.

The Networkwalks domain was used as the starting point for the investigation. Relevant transforms were applied to retrieve related information and visualize the discovered relationships.

The objective was to identify publicly available information associated with the target and understand how different entities could be connected.

### 5.2.3. Results and Observations

During the exercise, Maltego identified the following email address:

**info@networkwalks.com**

This result matched the email address obtained by the instructor during the corresponding practical exercise.

The result demonstrates that the investigation successfully reproduced the expected finding.

However, discovering an email address through OSINT does not confirm that the mailbox is currently active or that it can receive messages.

### 5.2.4. Security Relevance

Email addresses associated with an organization can provide useful information during reconnaissance.

They may reveal publicly exposed contact information and help security professionals understand the organization's digital presence.

At the same time, publicly available email addresses may be collected by malicious actors for spam, phishing or social engineering attempts.

Organizations should therefore monitor their publicly exposed information and ensure that employees are aware of email-based threats.

**Evidence:** [Insert Screenshot 7 – Maltego graph showing info@networkwalks.com]

---

## 5.3. Email and Host Discovery with theHarvester – W2-PM4

### 5.3.1. Overview

theHarvester is an OSINT tool used to collect publicly available information associated with a domain.

Depending on the selected data sources, it can retrieve information such as:

- Email addresses.
- Subdomains and hostnames.
- IP addresses.
- Associated URLs.
- Other publicly indexed information.

The objective of this exercise was to understand how theHarvester gathers information from different public sources and how the results can contribute to reconnaissance.

### 5.3.2. Initial Search Using Baidu

The first command executed was:

`theHarvester -d microsoft.com -l 1000 -b baidu`

The purpose was to collect publicly indexed information associated with the Microsoft domain using Baidu as the selected source.

**Results:**

The search did not return any IP addresses, email addresses, people or hosts.

This result does not mean that no information exists about the domain. It only indicates that the selected source did not return relevant results during this particular search.

**Evidence:** [Insert Screenshot 8 – Initial theHarvester search]

### 5.3.3. Search Using Multiple Data Sources

A second search was performed using multiple available data sources.

**Command used:**

`theHarvester -d microsoft.com -l 50 -b all`

The `-d` option specifies the target domain, `-l` sets the result limit, and `-b all` requests the available data sources supported by the tool.

During execution, several sources returned messages indicating that API keys were missing.

This means that some providers require an API key before their services can be queried. Consequently, not every source was able to return information.

Despite these limitations, the tool successfully collected information from some available sources.

### 5.3.4. Results and Observations

The main results displayed by theHarvester were:

| Information collected | Results |
|---|---:|
| Email addresses | 3 |
| IP addresses | 142 |
| Hosts | 9,960 |
| Autonomous System Numbers (ASNs) | 6 |
| Interesting URLs | 2 |
| People | 0 |
| LinkedIn profiles/users | 0 |

The tool also reported 44 hosts from the Hudson Rock source.

The following email addresses were identified:

1. dotnet-docker-bot@microsoft.com
2. opencode@microsoft.com
3. secure@microsoft.com

The Windvane source also reported 14 subdomains.

**Important interpretation note:**

These figures represent the aggregated results reported by the tool and its available data sources. They do not mean that all discovered IP addresses or hosts were independently verified as active, nor that every result necessarily belongs directly to Microsoft's operational infrastructure.

The statistics displayed by individual providers, including Hudson Rock, are source-specific statistics and should not be interpreted as the number of compromised Microsoft employees or accounts.

### 5.3.5. API Key Limitations

During the execution of the second command, several providers displayed messages indicating that API keys were missing.

This occurred because certain OSINT services require registered API credentials to access their databases.

The absence of an API key limited the amount of information available from those providers.

This does not necessarily indicate a problem with the Kali Linux installation or theHarvester itself. It is a limitation related to the access requirements of external data sources.

### 5.3.6. Security Relevance

TheHarvester demonstrates how publicly available information can be aggregated from different sources to build an initial picture of an organization's digital presence.

Email addresses, hostnames, IP addresses and subdomains can be useful to cybersecurity professionals during reconnaissance.

However, the same information could potentially be misused for phishing, social engineering or further unauthorized targeting.

For this reason, the information collected must be handled responsibly and should not be used to perform additional tests outside the authorized scope.

**Evidence:**

- [Insert Screenshot 9 – theHarvester command using Baidu]
- [Insert Screenshot 10 – theHarvester command using all sources]
- [Insert Screenshot 11 – theHarvester email addresses]
- [Insert Screenshot 12 – theHarvester summary statistics]

---

## 5.4. Network Discovery with Zenmap – W2-PM5

### 5.4.1. Overview

Zenmap is the graphical interface of Nmap, a network exploration and security auditing tool.

It can be used to identify devices on a network, discover active hosts and visualize network relationships.

The objective of this practical exercise was to perform network discovery in a controlled environment and understand how devices can be identified within a network.

### 5.4.2. Methodology

The network discovery exercise was performed using Zenmap.

The practical involved identifying the network configuration, selecting the appropriate network range and performing host discovery.

The scan was limited to the virtual machines used in the laboratory environment.

The objective was to identify the devices visible within the controlled environment rather than scan external networks.

**Network information:**

- Network range: [Insert your actual network range]
- Scanning tool: Zenmap
- Scan type: [Insert the scan profile used]
- Number of hosts discovered: [Insert your actual result]

### 5.4.3. Results and Observations

The network discovery exercise identified two virtual machines within the laboratory environment.

The machines were part of the controlled virtual network used for the practical exercise.

| Device | IP address | Role |
|---|---|---|
| Virtual Machine 1 | [Insert IP address] | [Insert operating system / role] |
| Virtual Machine 2 | [Insert IP address] | [Insert operating system / role] |

The results demonstrate how network discovery can help identify devices connected to a virtual network.

**Evidence:**

- [Insert Screenshot 13 – Zenmap scan configuration]
- [Insert Screenshot 14 – Zenmap scan results]
- [Insert Screenshot 15 – Zenmap topology, if generated]

# 6. RISK ANALYSIS AND POTENTIAL IMPACT

The information collected during the exercises highlights several potential security considerations.

The following table summarizes the main observations and their possible implications.

| No. | Observation | Potential impact | Suggested priority |
|---|---|---|---|
| 1 | Publicly available domain information | May help external parties understand an organization's digital presence. | Low |
| 2 | Email address identified through Maltego | Could potentially be misused for spam or phishing attempts. | Low |
| 3 | Multiple email addresses identified by theHarvester | May provide information that could be exploited in social engineering attempts. | Low |
| 4 | Hostnames and IP addresses collected from public sources | May help an attacker build an initial infrastructure map. | Medium |
| 5 | DNS and web technology information | May help identify technologies and services requiring further security review. | Medium |
| 6 | Devices discovered through local network scanning | Unknown devices may represent a potential network management or security concern. | Medium |

**Risk assessment limitation:**

The risk levels above are preliminary qualitative assessments based on the information collected during the exercises. They are not the result of a formal vulnerability assessment.

No confirmed vulnerability or successful compromise was established through these activities.

Information exposure alone does not prove that a system is vulnerable.

# 7. RECOMMENDATIONS

Based on the observations made during the practical exercises, the following recommendations can help organizations improve their security posture.

### 7.1. Monitor Publicly Available Information

Organizations should periodically review the information exposed through public sources, including domain registration details, email addresses, subdomains and other infrastructure-related information.

### 7.2. Protect Organizational Email Addresses

Employees should be trained to recognize phishing attempts and suspicious messages. Organizations should also implement appropriate email security controls.

### 7.3. Review Domain and DNS Configuration

DNS records should be reviewed regularly to ensure that only necessary information and services are publicly exposed.

### 7.4. Maintain an Updated Technology Inventory

Organizations should maintain an inventory of their web technologies, applications and infrastructure components to support security monitoring and maintenance.

### 7.5. Monitor External Infrastructure Exposure

Publicly exposed IP addresses, hostnames and subdomains should be reviewed to identify unexpected or unnecessary exposure.

### 7.6. Monitor Internal Networks

Organizations should periodically perform authorized network discovery to identify connected devices and maintain an accurate network inventory.

### 7.7. Investigate Unknown Devices

Any unexpected device discovered during internal network discovery should be investigated to determine whether it is legitimate and properly managed.

### 7.8. Use OSINT Responsibly

Information collected through OSINT tools should be analyzed carefully and used only for legitimate security purposes.

### 7.9. Respect Authorization Boundaries

Reconnaissance, scanning and security testing should always be performed within a clearly defined and authorized scope.

# 8. LIMITATIONS ENCOUNTERED

Several limitations were encountered during the practical activities.

**1. Data source availability**

Some theHarvester data sources required API keys. Their information could therefore not be retrieved during the exercise.

**2. Search engine limitations**

The initial Baidu search did not return relevant results. This demonstrates that different search sources may produce different results.

**3. Result validation**

Information collected through OSINT tools is not automatically verified. Email addresses, IP addresses and hostnames require additional validation before they can be considered confirmed findings.

**4. Scope of testing**

The activities were focused on information gathering and controlled network discovery. No exploitation or vulnerability validation was performed.

**5. Laboratory environment**

The Zenmap exercise was limited to the virtual machines used in the laboratory environment. Consequently, the results represent only the network configuration and devices visible during the exercise.

# 9. CONCLUSION

During Week 02 of the Networkwalks Cybersecurity Internship Program, I worked on practical activities related to footprinting, reconnaissance, OSINT and network discovery.

The use of Maltego helped me understand how publicly available information can be connected and visualized. I successfully identified the email address `info@networkwalks.com`, reproducing the result obtained by the instructor.

With theHarvester, I explored how different public data sources can be used to collect information associated with a domain. The exercise demonstrated that results depend on the selected sources and their availability. I also learned that API keys may be required to access certain providers and that collected information must be interpreted carefully.

The network discovery exercise with Zenmap provided practical experience in identifying devices within a controlled virtual network.

Overall, these activities helped me better understand the importance of reconnaissance in cybersecurity. They also demonstrated that publicly available information can provide valuable insights into an organization's digital presence, even before any active security assessment is conducted.

Finally, I learned that collecting information is only one part of the process. A cybersecurity professional must also know how to interpret findings, identify limitations, assess potential risks and document results accurately while respecting authorization boundaries.

# 10. EVIDENCE AND SCREENSHOTS

The following screenshots provide evidence of the practical activities performed during Week 02.

| Evidence | Description |
|---|---|
| Screenshot 1 | WHOIS results |
| Screenshot 2 | WhatWeb results |
| Screenshot 3 | Nslookup results |
| Screenshot 4 | cURL HTTP headers |
| Screenshot 5 | Wafw00f results |
| Screenshot 6 | DNSRecon results |
| Screenshot 7 | Maltego graph showing the discovered email address |
| Screenshot 8 | Initial theHarvester search using Baidu |
| Screenshot 9 | theHarvester search using multiple sources |
| Screenshot 10 | theHarvester email results |
| Screenshot 11 | theHarvester summary statistics |
| Screenshot 12 | Zenmap scan configuration and results |
| Screenshot 13 | Zenmap network topology, if available |

*Note: Adjust the screenshot numbering and descriptions to match the evidence actually included in the final report.*

---

**END OF REPORT**

**Program:** Networkwalks Cybersecurity Internship  
**Week:** 02  
**Report Topic:** Footprinting, OSINT and Network Discovery
