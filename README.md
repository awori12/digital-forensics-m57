# 🔍 Digital Forensic Investigation – M57.Biz Document Exfiltration
**Module:** CST2580 – Digital Incident Scene Investigation and Analysis  
**Institution:** Middlesex University Mauritius  
**Case Number:** CST2580-CW2-2025-001  
**Investigation Period:** February – April 2026  
**My Role:** Evidence Custodian

---

## 📋 Case Overview

This project involved a simulated digital forensic investigation into a suspected data exfiltration incident at M57.Biz, a fictional web start-up. A confidential salary spreadsheet (`m57biz.xls`) was discovered published on a competitor's website, originating from the laptop of the company's Chief Financial Officer (CFO), Jean.

The investigation aimed to determine:
- **How** the spreadsheet was exfiltrated
- **When** the incident occurred
- **Who** was responsible

---

## 🧑‍💼 My Role – Evidence Custodian (M00944397)

As Evidence Custodian, I was responsible for the integrity and legal defensibility of all physical and digital evidence:

- Opened and maintained the **Master Exhibit Register** before any evidence was collected
- Authored all **Chain of Custody (CoC)** documentation for four exhibits
- Wrote **contemporaneous notes** throughout the on-site investigation
- Physically recovered and documented **EX-001** (credential papers) and **EX-002** (USB flash drive)
- Witnessed the forensic imaging of Jean's laptop and verified **MD5 and SHA1 hash values**
- Ensured all procedures complied with **ACPO Principles** and **ISO/IEC 27037:2012**
- Supported digital analysis including email, file metadata, and USB artefact examination

---

## 🗂️ Evidence Collected

| Exhibit | Description | Key Finding |
|---|---|---|
| EX-001 | Papers with login credentials (Jean & Alison) | Found hidden beside a table — indicates credential compromise |
| EX-002 | USB Flash Drive (concealed in pipe under table) | Contained deleted `Credentials.txt` — evidence of data transfer |
| EX-003 | Forensic image of Jean's laptop (FTK Imager) | Source of spreadsheet, emails, and USB insertion trace |
| EX-004 | Jean's original laptop (sealed, preserved) | Maintains evidential integrity as source device |

---

## 🔬 Investigation Findings

### Key Artefacts Identified

- **`m57biz.xls`** found on Jean's desktop — hash values matched the file on the competitor's website, confirming it as the exact same file
- **MAC timestamps** showed the file was last accessed on **20 July 2008 at 05:28:00 MUT**
- **USB insertion** recorded at **05:26:18 MUT** on the same date — directly correlating with file access
- **Deleted `Credentials.txt`** recovered from USB image containing both Jean and Alison's passwords
- **Email analysis** revealed a coordinated phishing and spoofing attack via `tuckergeorge@gmail.com` impersonating internal accounts `alison@m57.biz` and `alex@m57.biz`

### Conclusion

Jean (CFO) was determined to be a **victim of social engineering**, not a perpetrator. The attacker used urgency, spoofed email identities, and credential theft to manipulate her into forwarding the spreadsheet. An external IP address (208.97.132.74) linked to dreamhost.com was associated with the third-party attacker.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| FTK Imager | Forensic imaging with write blocker |
| Autopsy | Email and file artefact analysis |
| AccessData FTK | Spreadsheet and metadata examination |
| Windows Command Line / Sleuth Kit | MAC time analysis (`mmls`, `fls`, `istat`, `icat`) |
| Kali Linux | Password cracking simulation (John the Ripper, zip2john) |
| OSINT Framework / Google Dorks | Open-source intelligence gathering |

---

## ⚖️ Standards & Legal Framework

| Standard / Law | Application |
|---|---|
| ACPO Principles | Evidence integrity and audit trail |
| ISO/IEC 27037:2012 | Digital evidence identification, collection, and preservation |
| ISO/IEC 27042:2015 | Analysis and interpretation of digital evidence |
| Computer Misuse Act 1990 | Legal basis for investigating unauthorised access |
| PACE Act 1984 | Search and seizure warrant procedures |
| Human Rights Act 1998 (Art. 8) | Privacy considerations during interviews |

---

## 🔐 Cybersecurity Recommendations

- Implement **Multi-Factor Authentication (MFA)** on all email accounts
- Deploy **email filtering** to detect phishing and spoofed senders (SPF, DKIM)
- Apply **Role-Based Access Control (RBAC)** for sensitive files
- Enforce **strong password policies** aligned with NIST SP 800-63B
- Implement **Data Loss Prevention (DLP)** controls for USB and email transfers
- Conduct regular **staff cybersecurity awareness training**

---

## 👥 Team

| Name | Student No. | Role |
|---|---|---|
| Marcellah Awori | M00944397 | Evidence Custodian |
| Suraya Kaiser | M00906631 | Project Manager |
| Kimberley Kiiza | M01005700 | Site Team Leader |
| Kinjal Govan | M01009459 | Forensic Examiner |

---

*Academic project submitted as part of BSc Cybersecurity and Digital Forensics, Middlesex University Mauritius.*
