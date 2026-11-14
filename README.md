 <div align="center">

# 🛡️ Penetration Testing – Footprinting & Network Scanning

**Performing domain reconnaissance, information gathering, DNS enumeration, and network discovery using Kali Linux tools and Zenmap.**

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Tool-Zenmap-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Focus-Footprinting-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Focus-Network%20Scanning-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Reconnaissance-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
</p>

---

## 📌 Project Overview

This project documents practical penetration testing activities covering **Footprinting, Reconnaissance, and Network Scanning** using Kali Linux tools and Zenmap.

The project consists of two practical modules completed as part of the Networkwalks Cybersecurity & Ethical Hacking Internship (Batch B084).

- **W2-PM1 – Multiple Kali Tools:** Performed domain footprinting and reconnaissance against `networkwalks.com` using six Kali Linux tools.
- **W2-PM5 – Zenmap Scanning:** Conducted network discovery on my own local LAN to identify active hosts, IP addresses, MAC addresses, and generate a network topology.

These activities demonstrate how cybersecurity professionals gather publicly available information and identify active devices during the initial phases of penetration testing.

---

## 🎯 Objectives

The main objectives of this project are to:

- Understand the footprinting and reconnaissance process.
- Collect publicly available domain registration information.
- Identify website technologies and server information.
- Resolve domain names into IP addresses using DNS.
- Analyze HTTP response headers.
- Detect Web Application Firewall (WAF) technology.
- Enumerate DNS records using DNSRecon.
- Identify local IP addresses and network subnets.
- Discover active hosts using Zenmap.
- Identify IP and MAC addresses of network devices.
- Generate and export network topology.
- Understand potential security risks and recommend improvements.

---

## 🛡️ Purpose of the Lab

These practical exercises provide hands-on experience with information gathering and network discovery.

They demonstrate how penetration testers and security professionals can:

- Collect publicly available domain information.
- Identify web technologies and server configurations.
- Analyze DNS infrastructure and records.
- Examine HTTP response headers.
- Identify Web Application Firewall technology.
- Discover active devices on a local network.
- Analyze network addresses and device information.
- Understand potential security exposures.
- Document findings and recommend security improvements.

⚠️ **Important:** All reconnaissance and scanning activities must be performed only on systems and networks where proper authorization has been obtained.

---

## 🏗️ Lab Outcomes

- Successfully completed two practical cybersecurity modules.
- Used six Kali Linux tools for domain footprinting and reconnaissance.
- Collected publicly available domain registration information using WHOIS.
- Identified website technologies using WhatWeb.
- Resolved domain IP information using Nslookup.
- Examined HTTP response headers using Curl.
- Identified ModSecurity using Wafw00f.
- Enumerated DNS records using DNSRecon.
- Discovered active hosts on my local LAN using Zenmap.
- Identified IP and MAC address information.
- Generated and exported a network topology in PDF format.
- Developed practical knowledge of reconnaissance, network scanning, and security risk identification.

---

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Windows 11 |
| 🐉 Reconnaissance OS | Kali Linux |
| 🌐 Target Domain | networkwalks.com |
| 🔎 Footprinting Tools | WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, DNSRecon |
| 🛠️ Scanning Tool | Zenmap (Nmap GUI) |
| 💻 Network Environment | Own Local LAN |
| 📡 Scan Type | Ping Scan |
| 🎯 Modules | W2-PM1 & W2-PM5 |
| 🔐 Focus | Footprinting & Network Discovery |

---

# 🪜 Practical Execution Procedure

## Step 1. Prepare the Kali Linux Environment

Opened Kali Linux and prepared the terminal environment for the footprinting and reconnaissance activities.

The practical involved using multiple command-line tools to gather publicly available information about the authorized target domain.

![](Screenshots/1-Kali-Linux.png)

---

## Step 2. Collect Domain Information Using WHOIS

Used WHOIS to collect publicly available domain registration information.

**Purpose:**
- Identify domain registration details.
- Examine domain name server information.
- Understand publicly available domain information.

**Command:**

```bash
whois networkwalks.com
```

![](Screenshots/2-WHOIS.png)

---

## Step 3. Identify Website Technologies Using WhatWeb

Used WhatWeb to identify the technologies and software used by the target website.

**Command:**

```bash
whatweb networkwalks.com
```

**Findings:**
- Identified WordPress 7.0.4.
- Identified WP Download Manager 3.3.58.
- Collected additional website technology information.

![](Screenshots/3-WhatWeb.png)

---

## Step 4. Resolve Domain IP Using Nslookup

Used Nslookup to resolve the target domain name into its corresponding IP address.

**Command:**

```bash
nslookup networkwalks.com
```

**Finding:**

```text
Target Domain: networkwalks.com
IP Address: 192.232.216.135
```

![](Screenshots/4-Nslookup.png)

---

## Step 5. Analyze HTTP Response Headers Using Curl

Used Curl with the `-I` option to inspect the HTTP response headers of the target website.

**Command:**

```bash
curl -I https://networkwalks.com
```

**Findings:**
- Inspected HTTP response headers.
- Collected web server information.
- Identified the WordPress REST API endpoint `/wp-json/`.

![](Screenshots/5-Curl.png)

---

## Step 6. Detect Web Application Firewall Using Wafw00f

Used Wafw00f to identify whether a Web Application Firewall was protecting the target website.

**Command:**

```bash
wafw00f https://networkwalks.com
```

**Finding:**

```text
Detected WAF: ModSecurity (SpiderLabs)
```

![](Screenshots/6-Wafw00f.png)

---

## Step 7. Enumerate DNS Records Using DNSRecon

Used DNSRecon to enumerate publicly available DNS records associated with the target domain.

**Command:**

```bash
dnsrecon -d networkwalks.com
```

**Findings:**
- Identified name server records.
- Examined mail server information.
- Collected SPF and TXT records.
- Examined service-related DNS records.
- Collected additional DNS infrastructure information.

![](Screenshots/7-DNSRecon.png)

---

## Step 8. Identify Local Network Configuration

Moved to the network scanning practical using Zenmap on Windows.

Opened Windows Command Prompt and executed the `ipconfig` command to identify the local IP address and network configuration.

**Command:**

```cmd
ipconfig
```

**Purpose:**
- Identify the local IPv4 address.
- Examine the subnet configuration.
- Determine the network range for scanning.

![](Screenshots/8-IPConfig.png)

---

## Step 9. Discover Live Hosts Using Zenmap

Opened Zenmap and entered the local network subnet identified through Windows CMD.

Selected **Ping Scan** to discover active devices on the local network.

**Scan Target (Example):**

```text
192.168.1.0/24
```

**Findings:**

Identified six live hosts in the practical results:

```text
192.168.1.1
192.168.1.3
192.168.1.4
192.168.1.6
192.168.1.8
192.168.1.254
```

![](Screenshots/9-Zenmap.png)

---

## Step 10. Identify MAC Addresses and Generate Network Topology

Examined the scan results to identify the MAC address information associated with discovered network devices.

Opened the **Topology** section in Zenmap and enabled the legend to visualize the discovered network devices.

Exported the generated network topology in PDF format as required by the practical.

**Activities Completed:**
- Examined discovered hosts.
- Identified available MAC address information.
- Opened the Zenmap Topology view.
- Enabled the topology legend.
- Generated the network topology.
- Exported the topology as a PDF file.

![](Screenshots/10-Network-Topology.png)

---

# 🔎 Practical Verification

| ✅ Test | 🧾 Tool / Command | 🎯 Expected Result |
|---|---|---|
| Domain registration | `whois` | Domain registration information |
| Website fingerprinting | `whatweb` | Website technologies identified |
| Domain resolution | `nslookup` | Target IP address |
| HTTP header inspection | `curl -I` | HTTP response headers |
| WAF detection | `wafw00f` | WAF identification |
| DNS enumeration | `dnsrecon` | DNS records |
| Local IP identification | `ipconfig` | Local IP and subnet |
| Network discovery | Zenmap Ping Scan | Active network hosts |
| MAC address identification | Zenmap | Available MAC addresses |
| Network topology | Zenmap Topology | Visual network map |

---

# 🐞 Problems Encountered & Solutions

Documenting problems and solutions is an important part of practical cybersecurity work.

## Problem 1. Understanding Different Footprinting Tools

- **Issue:** Each reconnaissance tool provided different types of information, making it necessary to understand their individual purposes and results.

- **Solution:** Used each tool separately and analyzed its output to understand domain registration, website technologies, DNS records, HTTP headers, and WAF information.

## Problem 2. Interpreting DNS Information

- **Issue:** DNSRecon returned multiple types of DNS records, including NS, MX, TXT, and service-related information.

- **Solution:** Examined the output and categorized the records to understand the target domain's DNS infrastructure.

## Problem 3. Identifying the Correct Local Network Range

- **Issue:** Zenmap required the correct local subnet to perform network discovery.

- **Solution:** Used Windows `ipconfig` to identify the local IPv4 address and subnet before entering the network range into Zenmap.

## Problem 4. Identifying Network Devices

- **Issue:** The network scan returned multiple active hosts, requiring further inspection to understand the discovered devices.

- **Solution:** Examined the Zenmap scan output and reviewed available IP and MAC address information.

## Problem 5. Generating Network Topology

- **Issue:** The network topology needed to be displayed clearly with its legend and saved in the required format.

- **Solution:** Opened Zenmap's Topology section, enabled the legend, and exported the topology as a PDF document.

---

# 💡 What I Learned

Through these practical activities, I developed an understanding of footprinting, reconnaissance, and network scanning.

The most important concepts I learned include:

### 1. Domain Footprinting

Learned how WHOIS provides publicly available domain registration and name server information.

### 2. Website Fingerprinting

Learned how WhatWeb identifies website technologies, CMS platforms, and plugins.

### 3. DNS Enumeration

Developed practical knowledge of Nslookup and DNSRecon for domain resolution and DNS record enumeration.

### 4. HTTP Header Analysis

Learned how Curl can inspect HTTP response headers and reveal additional information about web applications.

### 5. WAF Detection

Understood how Wafw00f can identify Web Application Firewall technologies.

### 6. Network Discovery

Learned how to use Zenmap to discover active hosts on a local network.

### 7. IP and MAC Address Identification

Developed an understanding of identifying network devices through their IP and MAC addresses.

### 8. Network Topology

Learned how to generate and export a visual representation of network devices using Zenmap.

### 9. Security Risk Assessment

Understood how information exposure and unknown network devices can create potential security concerns requiring further investigation.

---

# 📊 Risk Analysis & Recommendations

The practical activities highlighted several potential security observations:

| 🔍 Finding | ⚠️ Potential Impact | Risk Level |
|---|---|---|
| Web technology information exposed | Helps identify technologies for further security investigation | Medium |
| Server IP identifiable | Reveals network location information | Low |
| HTTP technical information exposed | Assists technology fingerprinting | Low |
| WAF technology identifiable | Reveals security architecture information | Low |
| DNS infrastructure information exposed | Helps build infrastructure profiles | Medium |
| Multiple live hosts visible | Unknown devices may be present on the network | Medium |

**Note:** These are potential risks based on reconnaissance observations, not confirmed vulnerabilities. No exploitation or vulnerability validation was performed.

### Recommended Security Improvements

- Regularly review publicly exposed technology information.
- Keep CMS platforms and plugins updated.
- Review HTTP response headers.
- Audit DNS records and publicly exposed services.
- Properly configure and monitor the Web Application Firewall.
- Perform regular internal network discovery.
- Investigate unknown network devices.
- Maintain updated network documentation.
- Conduct security testing only with proper authorization.

---

# 🔐 Security & Ethical Use

All activities documented in this repository were performed for educational and research purposes on systems and networks where written permission was secured or that I owned.

Unauthorized access, scanning, or testing of systems without proper permission is prohibited.

The findings documented in this project are observations from practical exercises and should not be considered proof of confirmed vulnerabilities.

---

# 🔗 Tools & Resources

- **Kali Linux:** https://www.kali.org/
- **Nmap / Zenmap:** https://nmap.org/
- **Networkwalks:** https://networkwalks.com/

---

# 👤 Author

**Zia Ur Rehman**  
Cybersecurity Intern – Batch B084

LinkedIn: [Zia Ur Rehman](https://www.linkedin.com/in/ziaurrehmanr05/)

---

## 📌 Project Information

**Program Name:** Cybersecurity Program at Networkwalks | **Week:** 02 | **Modules:** W2-PM1 (Multiple Kali Tools) & W2-PM5 (Zenmap Scanning) | **Project:** Penetration Testing – Footprinting & Network Scanning | **Repository:** GitHub
