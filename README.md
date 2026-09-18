# 🔐 SQROCK CYBERSECURITY INTERNSHIP — DAY 2

## 📧 Email Harvesting & Social Engineering Preparation

![Kali Linux](https://img.shields.io/badge/Kali_Linux-2026.2-557C94?logo=kalilinux\&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python\&logoColor=white)
![Requests](https://img.shields.io/badge/Requests-HTTP_Library-2.x-2C5AA0)
![Regex](https://img.shields.io/badge/Regex-Pattern_Matching-4B8BBE)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Security_Lab-red)
![Social Engineering](https://img.shields.io/badge/Social_Engineering-Awareness-orange)
![Ethical Hacking](https://img.shields.io/badge/Ethical_Hacking-Authorized_Lab-green)
![GitHub](https://img.shields.io/badge/GitHub-Documentation-181717?logo=github\&logoColor=white)

> **SQROCK IT Solution — Cybersecurity Internship Program**
> **Phase 1 | Week 1 | Day 2 | Beginner**

---

# 📌 Project Overview

This project was completed as part of **Day 2 of the SQROCK Cybersecurity Internship Program**.

The project focuses on **email harvesting and social-engineering preparation** in a controlled and authorized cybersecurity laboratory.

The objective was to develop a Python-based tool capable of retrieving the HTML content of an authorized webpage and identifying email addresses using **regular expressions (Regex)**.

For safety and ethical compliance, the exercise was performed against a **locally hosted laboratory webpage containing dummy email addresses**, rather than real individuals or organizations.

The project demonstrates how seemingly harmless publicly exposed information, such as email addresses, can potentially become an input into social-engineering reconnaissance.

---

# 🎯 Objectives

The main objectives of this project were to:

* Understand the concept of email harvesting.
* Understand the fundamentals of social engineering and pretexting.
* Develop a Python script for identifying email addresses in webpage content.
* Use the `requests` library to retrieve webpage content.
* Use Python's `re` module for regular-expression pattern matching.
* Remove duplicate email addresses from collected results.
* Save discovered addresses to an output file.
* Practice cybersecurity documentation and evidence collection.
* Understand the security risks associated with publicly exposed email addresses.
* Apply ethical and legal principles when performing security exercises.

---

# 🛠️ Tools and Technologies Used

| Tool / Technology      | Purpose                                    |
| ---------------------- | ------------------------------------------ |
| **Kali Linux**         | Cybersecurity laboratory operating system  |
| **Python 3**           | Development of the email-harvesting tool   |
| **Requests**           | Retrieving authorized webpage content      |
| **Regex (`re`)**       | Detecting email-address patterns           |
| **Python HTTP Server** | Hosting the local laboratory webpage       |
| **HTML**               | Creating the simulated target webpage      |
| **Linux Terminal**     | Executing commands and testing the project |
| **Git / GitHub**       | Version control and project documentation  |

---

# 🧠 Skills Demonstrated

This project demonstrates practical skills in:

* Python scripting
* Regular expressions
* HTTP requests
* HTML analysis
* Web-content processing
* Data extraction
* Duplicate-data removal
* File handling
* Linux command-line operations
* Basic OSINT concepts
* Social-engineering awareness
* Cybersecurity laboratory setup
* Security documentation
* Ethical hacking principles

---

# 🔬 Methodology

The project followed a controlled laboratory workflow:

```text
┌───────────────────────────┐
│  Create Local Lab Page    │
│   with Dummy Emails       │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│   Start Python HTTP       │
│       Server              │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ Python Requests Library   │
│ Retrieves HTML Content    │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ Regex Searches HTML for   │
│ Email Address Patterns    │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ Remove Duplicate Emails   │
│       Using Set()         │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ Display & Save Results    │
│  harvested_emails.txt     │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ Security & Social         │
│ Engineering Analysis      │
└───────────────────────────┘
```

### Step 1 — Laboratory Website Creation

A simple HTML webpage was created containing dummy email addresses.

Example:

```text
alice@example.test
bob@example.test
security@example.test
training@example.test
```

These addresses were created exclusively for cybersecurity training.

### Step 2 — Local Web Server

The webpage was hosted locally using Python's built-in HTTP server:

```bash
python3 -m http.server 8000
```

The laboratory website was then accessible through:

```text
http://127.0.0.1:8000
```

### Step 3 — HTTP Content Retrieval

The Python `requests` library was used to retrieve the HTML content:

```python
response = requests.get(url, timeout=10)
```

### Step 4 — Email Pattern Detection

A regular expression was used to identify strings matching common email-address patterns:

```python
pattern = r'[\w.+-]+@[\w-]+\.[a-zA-Z]{2,}'
```

### Step 5 — Duplicate Removal

The extracted results were converted into a Python `set`:

```python
emails = set(re.findall(pattern, html))
```

This prevented duplicate email addresses from appearing multiple times.

### Step 6 — Results Storage

The discovered addresses were saved to:

```text
harvested_emails.txt
```

### Step 7 — Security Analysis

The results were analyzed from both attacker-awareness and defensive perspectives.

The exercise demonstrated that publicly exposed email addresses can potentially be used as one component of social-engineering reconnaissance.

---

# 🧪 Laboratory Environment

The project was performed in an **isolated Kali Linux virtual laboratory environment**.

### Laboratory configuration

```text
Host Machine
     │
     ▼
VirtualBox
     │
     ▼
Kali Linux VM
     │
     ├── Python 3
     │
     ├── Email Harvester
     │
     └── Local HTTP Server
              │
              ▼
       Local Lab Web Page
       (Dummy Data Only)
```

The exercise did not target real individuals, organizations, or unauthorized infrastructure.

---

# ⚙️ Environment Configuration

### Operating System

```text
Kali Linux
```

### Python

```bash
python3 --version
```

### Project Directory

```bash
mkdir -p ~/sqrock-internship/day2-email-harvesting
cd ~/sqrock-internship/day2-email-harvesting
```

<img width="665" height="523" alt="project 2 directory created" src="https://github.com/user-attachments/assets/8737adfe-f3d8-4bb2-9ce4-2c5e67087764" />


### Required Python Library

The project uses:

```python
import requests
import re
```

If `requests` is not installed:

```bash
sudo apt update
sudo apt install python3-requests -y
```

### Local Web Server

```bash
python3 -m http.server 8000
```

<img width="625" height="144" alt="build and authorize local web server" src="https://github.com/user-attachments/assets/1f2ce2ee-3839-49db-a1b1-18499735bacf" />


### Test URL

```text
http://127.0.0.1:8000/lab_page.html
```

---

# 📁 Project Structure

```text
Day-02-Email-Harvesting/
│
├── email_harvester.py
│
├── lab_page.html
│
├── harvested_emails.txt
│
├── screenshots/
│   ├── 01-project-directory.png
│   ├── 02-lab-website.png
│   ├── 03-python-script.png
│   ├── 04-script-execution.png
│   └── 05-harvested-results.png
```

### File Description

| File                   | Description                         |
| ---------------------- | ----------------------------------- |
| `email_harvester.py`   | Python email extraction tool        |
| `lab_page.html`        | Local webpage containing dummy data |
| `harvested_emails.txt` | Extracted email addresses           |
| `screenshots/`         | Evidence of project execution       |
| `README.md`            | Project documentation               |

---

# 📊 Sample Results

The laboratory webpage contained four dummy email addresses.

The script successfully identified:

```text
alice@example.test
bob@example.test
security@example.test
training@example.test
```

Example terminal output:

```text
=======================================================
SQROCK DAY 2 - EMAIL HARVESTING LAB
=======================================================
[+] Target: http://127.0.0.1:8000/lab_page.html
[+] Scope: Authorized local laboratory

[+] Emails discovered: 4

    alice@example.test
    bob@example.test
    security@example.test
    training@example.test

[+] Results saved to harvested_emails.txt

---

# 🛡️ Security Analysis

Email harvesting can be relevant to social-engineering attacks because an exposed email address can provide attackers with an initial piece of information about a potential target.

A simplified attack chain can be represented as:

```text
Public Information
       ↓
Email Discovery
       ↓
Target Research
       ↓
Pretext Development
       ↓
Social Engineering Attempt
       ↓
Potential Credential / Information Theft
```

<img width="651" height="289" alt="email harvesting script created and run" src="https://github.com/user-attachments/assets/cb12febe-01de-4972-925c-87d46b3a892d" />

The email address alone does not indicate that an account has been compromised. However, it may become more useful to an attacker when combined with additional information from other public sources.

---

# 🔐 Defensive Measures

Organizations can reduce risks associated with exposed email addresses by implementing:

### 1. Email Exposure Management

Avoid unnecessarily publishing employee contact information.

### 2. Multi-Factor Authentication

MFA can provide an additional security layer if passwords are compromised.

### 3. Security Awareness Training

Employees should be trained to recognize suspicious emails and social-engineering attempts.

### 4. SPF, DKIM and DMARC

Email authentication technologies can help organizations reduce email spoofing and improve domain protection.

### 5. Monitoring

Security teams should monitor authentication activity and investigate unusual behavior.

### 6. Least Privilege

Employees should only receive access necessary for their responsibilities.

---

# 🎓 Learning Outcomes

After completing this project, I gained practical experience in:

* Understanding email harvesting concepts.
* Using Python for basic cybersecurity automation.
* Working with the `requests` library.
* Applying regular expressions to web content.
* Extracting structured information from HTML.
* Removing duplicate results using Python sets.
* Writing results to files.
* Running a local HTTP server.
* Performing security exercises in an authorized environment.
* Understanding how publicly available information can support social-engineering reconnaissance.
* Thinking about cybersecurity from both attacker-awareness and defensive perspectives.
* Documenting cybersecurity projects professionally.

---

# ⚠️ Challenges Faced and How They Were Overcome

## Challenge 1 — Working Safely With Email Data

Using real people's email addresses could create privacy and authorization concerns.

### Solution

A local laboratory webpage was created containing dummy email addresses.

This allowed the harvesting technique to be demonstrated without targeting real individuals.

---

## Challenge 2 — Understanding Regular Expressions

Initially, email-address patterns can be difficult to understand because Regex uses special characters and syntax.

### Solution

The pattern was broken down into individual components:

```text
[\w.+-]+
@
[\w-]+
\.
[a-zA-Z]{2,}
```

This made it easier to understand how the program identifies potential email addresses.

---

## Challenge 3 — Duplicate Results

A webpage may contain the same email address multiple times.

### Solution

Python's `set()` data structure was used:

```python
emails = set(re.findall(pattern, html))
```

This automatically removes duplicate values.

---

## Challenge 4 — Connecting the Script to the Laboratory Website

The Python script needed an accessible webpage from which to retrieve HTML.

### Solution

Python's built-in HTTP server was used:

```bash
python3 -m http.server 8000
```

This provided a simple local web environment for testing.

---

# ⚖️ Ethical and Legal Considerations

This project was conducted strictly within an **authorized cybersecurity laboratory environment**.

The following principles were followed:

* No unauthorized systems were targeted.
* No real individuals were targeted.
* Dummy email addresses were used.
* No credentials were collected.
* No phishing messages were sent.
* No malicious payloads were deployed.
* The exercise was performed for cybersecurity education and awareness.

> **Authorized systems only. Never perform email harvesting, phishing, or social-engineering activities against systems or individuals without explicit authorization.**

---

# 📌 Conclusion

The SQROCK Day 2 project provided practical experience in **email harvesting, Python automation, Regex-based pattern matching, and social-engineering awareness**.

By building the tool inside a controlled Kali Linux laboratory, I was able to understand how email addresses can be extracted from webpage content while maintaining appropriate ethical and legal boundaries.

The project also reinforced the importance of reducing unnecessary information exposure and implementing security controls such as **MFA, email authentication, security awareness training, and monitoring**.

---

 # 👤 Author
  Atemlefac Nkafu Bechem
  
  Cybersecurity Engineer

LinkedIn: https://www.linkedin.com/in/atemlefac-nkafu-bechem-179987248

# 📌 Project Information
**Program Name:** Cybersecurity internship at SQROCK | **Week:** 01 | **Project 2:** Email harvesting and social engineering | **Repository:** GitHub
