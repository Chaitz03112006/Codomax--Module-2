# 🔐 Module 02 – Day 09: Cybersecurity Tools & Network Traffic Analysis

## 📌 Overview

This repository documents my Day 9 practical activities as part of my Cybersecurity Training.

The practical focuses on learning and exploring three important cybersecurity tools:

- **Wireshark** – Network packet capturing and analysis.
- **Burp Suite** – Web application traffic inspection.
- **OWASP ZAP** – Web application security testing.

The exercises were performed in a controlled Kali Linux environment using a local test website.

## 🎯 Objectives

1. Understand network packet analysis.
2. Capture and analyze ICMP packets using Wireshark.
3. Understand HTTP requests and responses.
4. Inspect web traffic using Burp Suite.
5. Explore web application security testing using OWASP ZAP.
6. Understand the importance of safe and authorized security testing.

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Cybersecurity testing environment |
| Wireshark | Network packet analysis |
| Burp Suite Community Edition | HTTP traffic inspection |
| OWASP ZAP | Web application security testing |
| Python | Creating a local test web server |
| Firefox | Accessing the local test website |

## 📚 Practical Activities

### 1. Wireshark – Network Packet Analysis

**Objective:** Capture and analyze network packets.

Activities performed:
- Opened Wireshark in Kali Linux.
- Selected the Loopback (`lo`) interface.
- Generated network traffic using the ping command.
- Applied the ICMP display filter.
- Identified ICMP Echo Request and Echo Reply packets.
- Inspected packet details and saved the capture file.

**Command used:**

```bash
ping -c 4 127.0.0.1
```

**Wireshark display filter:**

```text
icmp
```

**Output file:** `Day09_Wireshark.pcapng`

### 2. Burp Suite – Web Traffic Inspection

**Objective:** Understand HTTP communication between a browser and a web server.

Activities performed:
- Started Burp Suite.
- Checked the proxy listener configuration.
- Configured Firefox to use the local proxy.
- Created a local test website using Python.
- Accessed the website through Firefox.
- Inspected HTTP requests and responses using HTTP History.

**Commands used:**

```bash
mkdir -p ~/Module02_Lab/Day09_Burp
cd ~/Module02_Lab/Day09_Burp

echo '<h1>My Cybersecurity Test Website</h1><p>Burp Suite Practical</p>' > index.html

python3 -m http.server 8000 --bind 127.0.0.1
```

**Local test website:**

```text
http://127.0.0.1:8000
```

**Burp proxy configuration:**

```text
IP Address: 127.0.0.1
Port: 8080
```

### 3. OWASP ZAP – Web Application Security Testing

**Objective:** Explore a local web application and inspect potential security findings.

Activities performed:
- Opened OWASP ZAP.
- Used the Manual Explore feature.
- Accessed the local test website.
- Explored the Sites panel.
- Inspected HTTP requests and responses.
- Reviewed the Alerts panel.

**Target URL:**

```text
http://127.0.0.1:8000
```

Passive inspection was used for this beginner-level exercise.

## 📸 Screenshots & Evidence

Screenshots are included to document the practical activities and their outputs.

Suggested screenshot organization:

```text
Module02_Lab/
│
└── Day09/
    │
    ├── Wireshark/
    │   ├── Screenshot_01_Interface.png
    │   ├── Screenshot_02_Ping.png
    │   ├── Screenshot_03_ICMP_Packets.png
    │   └── Screenshot_04_Packet_Details.png
    │
    ├── Burp_Suite/
    │   ├── Screenshot_01_Burp_Home.png
    │   ├── Screenshot_02_Proxy_Settings.png
    │   └── Screenshot_03_HTTP_History.png
    │
    └── OWASP_ZAP/
        ├── Screenshot_01_ZAP_Home.png
        ├── Screenshot_02_Sites_Panel.png
        └── Screenshot_03_Alerts.png
```

## 📖 Key Learnings

- Understood how network packets are captured and analyzed.
- Learned the difference between ICMP Echo Request and Echo Reply.
- Understood the role of proxy servers in web communication.
- Learned how to inspect HTTP requests and responses.
- Explored the basic features of OWASP ZAP.
- Practised using cybersecurity tools in a controlled environment.

## 🔒 Security & Ethical Considerations

All practical exercises were performed on my own Kali Linux environment and local test website.

- No unauthorized systems were scanned.
- No third-party private traffic was intercepted.
- No real user credentials or sensitive information were used.
- Active security testing should only be performed with proper authorization.

## 📝 Conclusion

Successfully explored three important cybersecurity tools: Wireshark, Burp Suite and OWASP ZAP.

This practical provided hands-on experience in network packet analysis, HTTP traffic inspection and basic web application security testing.

It helped strengthen my understanding of practical cybersecurity concepts and the tools commonly used by security professionals.

---

**Training Module:** Module 02 – Linux, Security Tools & Reconnaissance  
**Practical:** Day 09  
**Environment:** Kali Linux (VirtualBox)  
**Focus:** Network Analysis & Web Application Security

⭐ *Learning cybersecurity one practical at a time!*
