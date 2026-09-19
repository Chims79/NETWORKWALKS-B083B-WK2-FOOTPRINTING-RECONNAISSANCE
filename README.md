<div align="center">

# 🔐 Cybersecurity- Reconnaissance and Footprinting

**A guide to penetration testing and ethical hacking practice**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Chimanda%20Mbangweta%20CyberSecurity%20Specialist-C00000?style=flat-square" />
</p>

---

## 📌 Project Overview

In this project, the focus is on the very first steps in **hacking,** and in this case, passive **ethical hacking or penetration testing using VirtualBox and Kali Linux.**

The main purpose is to show how information is first collected from the target system or organization and the steps that lead to vulnerability assessment and exploitation using a number of cybersecurity tools and skills in Kali Linux.

---

## 🎯 Objectives

The main objectives of this project are to:

Carry out reconnaissance and foot printing using the following tools in kali linux;

|⚙️Tool      |  🎯  Result|
|------------|-------------|
|**whois** | Identify domain registration details| 
|**whatWeb**|     fingerprinting the Web technology running on the system|
|**nslookup**|     DNS / IP resolution| 
|**curl -i** |       Read the HTTP response headers to see the server banner, status, cookies and redirects|
|**wafw00f** |       Identify and security measures put in place like firewalls|
|**dnsrecon**|      Enumerate all DNS records|
|**Zenmap** | Network scanning and mapping|

---

## 🧪 Methodology and steps taken

 1.  **whois.**
    
       *Querying the public domain registration record to find who owns the domain, when it was registered, and its name servers (networkwalks).*

![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%20_16_09_2026_23_29_40.png)


---


2. **whatweb.**

     *Fingerprint the technologies running on the website: web server, CMS, plugins, frameworks and IP address.*

   ![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%201_18_09_2026_00_54_42.png)

   
  --- 


3. **nslookup.**

     *Resolve the domain name to its IP address using DNS.*

   ![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%201_18_09_2026_01_00_09.png)

   
   ---


4. **curl -I.**

     *Read the HTTP response headers to see the server banner, status, cookies and redirects.*

   ![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%201_18_09_2026_01_27_48.png)
   

   ---


5. **wafw00f.**

   *Detect whether a Web Application Firewall (WAF) is protecting the target site.*


   ![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%201_18_09_2026_01_23_47.png)
   

---


6. **dnsrecon.**

     *Enumerate all DNS records: name servers, mail servers, SPF, TXT and service (SRV) records.*


   ![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/153d2429dfdd10f948c0f7222e6617058fa06d1a/VirtualBox_Kali%201_18_09_2026_01_36_19.png)

   ---


7. **zenmap**

 ### Live Host Identification on the 10.0.0.0/24 Subnet using Zenmap / Nmap
---
|Activity|Result|
|--------------|-------------|
|Subnet Scanned|	10.0.0.0/24|
|Scan Type (Discovery)|	nmap -sn 10.0.0.0/24  (Ping Scan)|
|Follow-up Scans|	nmap -T4 -A -v <host>  (Intense/Service+OS Detection Scan)|
|Total Addresses| Probed	256|
|Live Hosts Found|	4|
|Scan Duration (Ping Scan)|	2.09 seconds|

This report documents a live host discovery exercise performed with Zenmap (the graphical front-end for Nmap). A ping sweep of the local subnet was used to identify which addresses were online, followed by targeted intense scans against each discovered host to gather service, OS and MAC address detail. Screenshots of every scan are included as evidence.
 
### Live Hosts / PCs Found in the Subnet
A ping scan (nmap -sn 10.0.0.0/24) was run from Zenmap's built-in terminal to sweep every address in the subnet without port-scanning each host. Nmap reported that out of 256 possible addresses, 4 hosts responded and are therefore "live" on the network:

|No.	|IP Address|	MAC Address	Vendor / NIC|	Notes|
|---  |----------|--------------------------|------|
|1	|10.0.0.1|	52:54:00:12:35:00	|QEMU virtual NIC|	Gateway / router (localhost's host)|
|2	|10.0.0.2|	-- (local interface)|	--	Scanning machine itself| (no MAC reported for self)|
|3	|10.0.0.9|	08:00:27:51:76:01|	Oracle VirtualBox virtual NIC |Android device - port 5555/tcp (adb) open||
|4	|10.0.0.11|	08:00:27:35:58:1A|	Oracle VirtualBox virtual NIC|	VirtualBox VM host|

![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/370cbc3b95627537db6a3b71eadc78055f85b4d0/Zen3.png)
                               *Figure 1 - Zenmap ping scan (nmap -sn 10.0.0.0/24) showing 4 live hosts out of 256 addresses.*





                               


![image alt](https://github.com/Chims79/NETWORKWALKS-B083B-WK2-FOOTPRINTING-RECONNAISSANCE/blob/370cbc3b95627537db6a3b71eadc78055f85b4d0/Topology.png)
                                     *Figure 2 - Zenmap Topology* 




                                     
 

 
## How Many Hosts Are Live in the Subnet?


4 hosts responded as "up" out of the 256 addresses scanned in the 10.0.0.0/24 subnet, as confirmed by Nmap's summary line at the end of the ping scan: "Nmap done: 256 IP addresses (4 hosts up) scanned in 2.09 seconds."




 

## IP Addresses of the Live Hosts

The four live hosts identified were:
●	10.0.0.1

●	10.0.0.2

●	10.0.0.9

●	10.0.0.11

These same four addresses also appear as nodes in the Zenmap Topology map (Figures 2 and 3), connected to the scanning host (localhost).



 
## MAC Addresses of the Live Hosts

Nmap resolves MAC addresses for hosts on the same local Ethernet segment via ARP. The ping scan output returned the following MAC addresses for three of the four hosts (the fourth, 10.0.0.2, is the scanning machine's own interface, so Nmap does not report a MAC address for itself):
|IP Address|	MAC Address|
|----------|-------------|
|10.0.0.1|	52:54:00:12:35:00|
|10.0.0.2|	Not reported|
|10.0.0.9|	08:00:27:51:76:01|
|10.0.0.11|	08:00:27:35:58:1A|


---



### 💡 Key Takeaways

- The exercise showed that information gathering is an important and fundamental part of cybersecurity that must be used to carefully analyse publicly available information and network responses.
- technical findings should be always documented clearly
- reconnaissance and scanning must always be performed within an authorized scope.

  ---

  ## Report

  

  ## ⚖️ Disclaimer

The information provided here is meant solely for learning and legitimate and sanctioned research purposes. Note that accessing any computer system(s) without proper consent is a criminal offense in most legal jurisdictions. Every task outlined in this document was carried out exclusively on infrastructure I personally own, networks under my own control, or systems for which I had clear, written approval to test. 



# 👤 Author

**Chimanda P Mbangweta**

Cybersecurity Professional B083B

LinkedIn:  https://www.linkedin.com/in/chimanda-p-mbangweta-45972772

________________________________________
# 📌Project Information
**Program Name:** *Cybersecurity at Networkwalks | **Week:** 01 | **Project:** Cybersecurity & Pen testing Lab Setup | **Repository:** GitHub*


---
 
 
