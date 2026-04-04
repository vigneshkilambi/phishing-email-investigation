# 🚨 Phishing Email Investigation with Network Traffic Analysis

### 👤 Vignesh Kilambi | Aspiring SOC Analyst

---

## 📌 Overview

This project demonstrates a real-world phishing email investigation conducted in a SOC environment. The analysis includes email inspection, header analysis, IOC extraction, and network traffic investigation using Wireshark to identify malicious activity and potential credential harvesting.

---

## 🛠️ Tools Used

* Kali Linux
* Wireshark
* MXToolbox

---

## 🔍 Investigation Process

### 📧 Phishing Email Analysis

* Identified suspicious sender email (domain mismatch)
* Detected malicious link embedded in email content
* Observed social engineering techniques to trick the user

### 📨 Email Header Analysis

* SPF, DKIM, and DMARC authentication failed
* Sender IP identified as suspicious
* Confirmed spoofed phishing email

### 🧪 IOC Extraction

* Extracted malicious indicators from email and traffic
* Identified domains, IP address, URL, and file involved

### 🌐 Network Traffic Analysis (Wireshark)

#### DNS Analysis

* Observed DNS query for malicious domain
* Domain resolution confirms attacker infrastructure

#### HTTP Analysis

* Detected HTTP request to phishing domain
* JavaScript file retrieved (`loginDialog.js`)
* Indicates credential harvesting behavior

---

## 🔗 Attack Flow

Phishing Email
↓
User clicks malicious link
↓
DNS request → servervirto.com.co
↓
HTTP request → phishing page
↓
JavaScript loaded (loginDialog.js)
↓
Credentials captured

---

## 🧠 MITRE ATT&CK Mapping

* T1566 – Phishing
* T1204 – User Execution
* T1071 – Web Communication

---

## ⚠️ Impact

* Credential theft possible
* Unauthorized account access
* Risk of sensitive data compromise

---

## 📊 Indicators of Compromise (IOCs)

| Type   | Value                                                              |
| ------ | ------------------------------------------------------------------ |
| Email  | [sues@nnwifi.com](mailto:sues@nnwifi.com)                          |
| Domain | nnwifi.com                                                         |
| IP     | 94.100.31.27                                                       |
| Domain | servervirto.com.co                                                 |
| URL    | http://servervirto.com.co/ed/trn/update/login_files/loginDialog.js |
| File   | loginDialog.js                                                     |

---

## 📊 Evidence

* Phishing email sample (.eml)
* Extracted IOCs
* Wireshark network traffic screenshots

---

## 📁 Project Structure

phishing-email-investigation/
│
├── README.md
├── Phishing_Email_Investigation.pptx
│
├── email-sample/
│   └── phishing_sample.eml
│
├── ioc/
│   └── iocs.txt
│
├── screenshots/
│
└── pcap/ (optional)

---

## 👤 Author

**Vignesh Kilambi**
Aspiring SOC Analyst
