
---

## 🚀 Phase 0 — Setup

> **Goal:** Understand both platforms, set up your environment, and build study habits.

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? | ⏱️ |
|:---:|:---|:---:|:---|:---|:---:|
| 0.1 | [How to use TryHackMe](https://tryhackme.com/room/howtousetryhackme) | 🟦 THM | None | Launch AttackBox, connect via OpenVPN, understand answer submission. | 45 min |
| 0.2 | [Pre Security Path](https://tryhackme.com/path/outline/presecurity) | 🟦 THM | 0.1 | Networking, OS, and web basics (HTML/CSS/JS) in simple terms. | ~15 h |
| 0.3 | [HTML - Source code](https://www.root-me.org/en/Challenges/Web-Client/HTML-Source-code) | 🟥 RM | Basic HTML (from 0.2) | Proves that understanding HTML structure is a prerequisite for any security test. | 5 min |
| 0.4 | [OpenVPN](https://tryhackme.com/room/openvpn) | 🟦 THM | 0.1 | Set up a secure connection to the platform (if not using AttackBox). | 45 min |

> ✅ **Transition criterion:** You can launch AttackBox or connect via OpenVPN, and solve `HTML - Source code` without help.

---

## 🌐 Phase 1 — Web Foundations (Before Any Vulnerability!)

> **Golden rule:** Do not touch Root Me's web challenges until you understand HTML, HTTP, and JavaScript.

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? | ⏱️ |
|:---:|:---|:---:|:---|:---|:---:|
| 1.1 | [How Websites Work](https://tryhackme.com/room/howwebsiteswork) | 🟦 THM | 0.2 | Distinguishes HTML (structure), CSS (style), and JS (interaction). | 45 min |
| 1.2 | [HTTP in Detail](https://tryhackme.com/room/httpindetail) | 🟦 THM | 1.1 | Request/response cycle, headers, GET/POST. **Without HTTP, there is no XSS or SQLi.** | 30 min |
| 1.3 | [JavaScript Basics](https://tryhackme.com/room/javascriptbasics) | 🟦 THM | 1.1 | **🔒 Prerequisite for XSS:** DOM, events, element manipulation. | 1 h |
| 1.4 | [Javascript - Authentication](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Authentication) | 🟥 RM | 1.3 | Analyze JS to reach protected data. | 10 min |
| 1.5 | [Javascript - Obfuscation 1](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-1) | 🟥 RM | 1.3 | Read obfuscated JS — a core skill for web analysis. | 15 min |
| 1.6 | [HTML - From the outside](https://www.root-me.org/en/Challenges/Web-Server/HTML-From-the-outside) | 🟥 RM | 1.1 + 1.2 | Spot information leakage via HTML comments. | 5 min |
| 1.7 | [HTTP - IP restrict access](https://www.root-me.org/en/Challenges/Web-Server/HTTP-IP-restrict-access) | 🟥 RM | 1.2 | Manipulate headers (`X-Forwarded-For`). | 10 min |
| 1.8 | [HTTP - User-agent](https://www.root-me.org/en/Challenges/Web-Server/HTTP-User-agent) | 🟥 RM | 1.2 | User-Agent is an input, not just metadata. | 10 min |
| 1.9 | [Burp Suite: The Basics](https://tryhackme.com/room/burpsuitebasics) | 🟦 THM | 1.2 | Intercept and modify requests — essential for everything that follows. | 1 h |

> ✅ **Transition criterion:** You can intercept a request, understand it, and modify it manually in Burp without help.

---

## 🎯 Phase 2 — First Vulnerabilities: XSS & SQLi

> **Goal:** Exploit your first real vulnerabilities, understanding the **root cause**, not just running a tool.

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? | ⏱️ |
|:---:|:---|:---:|:---|:---|:---:|
| 2.1 | [Intro to Cross-site Scripting](https://tryhackme.com/room/xss) | 🟦 THM | **1.3 (JavaScript) complete** | XSS types: Reflected, Stored, DOM-based. | 2 h |
| 2.2 | [XSS - Reflected](https://www.root-me.org/en/Challenges/Web-Client/XSS-Reflected) | 🟥 RM | 2.1 | Exploit reflected XSS to steal a cookie in a real scenario. | 15 min |
| 2.3 | [XSS - Stored 1](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-1) | 🟥 RM | 2.2 | Understand Reflected vs. Stored in practice. | 20 min |
| 2.4 | [SQL Injection Introduction](https://tryhackme.com/room/sqlinjectionlm) | 🟦 THM | 1.2 + SQL basics (from 0.2) | How input influences database queries. | 1 h |
| 2.5 | [SQL injection - Authentication](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Authentication) | 🟥 RM | 2.4 | Bypass a login form in practice. | 15 min |
| 2.6 | [SQL injection - String](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-String) | 🟥 RM | 2.5 | Data extraction via string input. | 15 min |
| 2.7 | [SQL injection - Numeric](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Numeric) | 🟥 RM | 2.5 | Data extraction via numeric input (UNION-based). | 20 min |

> ✅ **Transition criterion:** You solve XSS and SQLi challenges on Root Me without copying solutions.

---

## 🧩 Phase 3 — Advanced Web Vulnerabilities

> **Goal:** Build a full exploit chain: CSRF, file upload, command injection, LFI/RFI — the path to your **first real shell**.

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? | ⏱️ |
|:---:|:---|:---:|:---|:---|:---:|
| 3.1 | [CSRF Introduction](https://tryhackme.com/room/csrfintroduction) | 🟦 THM | 1.2 + 1.3 | Understand the browser's trust in a session. | 1 h |
| 3.2 | [CSRF - 0 protection](https://www.root-me.org/en/Challenges/Web-Client/CSRF-0-protection) | 🟥 RM | 3.1 | Direct application. | 15 min |
| 3.3 | [CSRF - token bypass](https://www.root-me.org/en/Challenges/Web-Client/CSRF-token-bypass) | 🟥 RM | 3.2 | Bypass token protection (needs JS + HTTP). | 20 min |
| 3.4 | [File Upload Vulnerabilities](https://tryhackme.com/room/uploadvulns) | 🟦 THM | 1.2 + PHP basics | Bypass upload filters to reach RCE. | 1 h |
| 3.5 | [File upload - Double extensions](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Double-extensions) | 🟥 RM | 3.4 | Bypass a filter with a double extension. | 15 min |
| 3.6 | [File upload - MIME type](https://www.root-me.org/en/Challenges/Web-Server/File-upload-MIME-type) | 🟥 RM | 3.5 | Bypass MIME-type filters via Burp. | 15 min |
| 3.7 | [File upload - Null byte](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Null-byte) | 🟥 RM | 3.6 | Bypass a filter using a null byte. | 20 min |
| 3.8 | [Command Injection](https://tryhackme.com/room/oscommandinjection) | 🟦 THM | 1.2 + Linux basics | OS command injection. | 1 h |
| 3.9 | [Command injection - Basic](https://www.root-me.org/en/Challenges/Web-Server/Command-injection-Basic) | 🟥 RM | 3.8 | Direct application. | 15 min |
| 3.10 | [Command injection - Blind](https://www.root-me.org/en/Challenges/Web-Server/Command-injection-Blind) | 🟥 RM | 3.9 | Blind injection (time-based). | 30 min |
| 3.11 | [LFI - Local File Inclusion](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion) | 🟥 RM | 1.2 + 3.8 | Read system files via path traversal. | 20 min |
| 3.12 | [LFI - Journey through files](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion-Journey-through-files) | 🟥 RM | 3.11 | Escalate LFI to read sensitive files. | 30 min |
| 3.13 | [RFI - Remote File Inclusion](https://www.root-me.org/en/Challenges/Web-Server/Remote-File-Inclusion) | 🟥 RM | 3.11 | Include a remote file to obtain a shell. | 30 min |
| 3.14 | [Backup files](https://www.root-me.org/en/Challenges/Web-Server/Backup-files) | 🟥 RM | 1.2 | Discover leftover backup files (recon skill). | 15 min |
| 3.15 | [Weak password](https://www.root-me.org/en/Challenges/Web-Server/Weak-password) | 🟥 RM | 1.2 | Smart guessing of weak passwords. | 20 min |

> ✅ **Transition criterion:** You obtain a shell (reverse or web shell) on Root Me without a walkthrough.

---

## 🖥️ Phase 4 — System Exploitation & Privilege Escalation

> **Goal:** After getting a shell, how do you reach root/SYSTEM?

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? | ⏱️ |
|:---:|:---|:---:|:---|:---|:---:|
| 4.1 | [Linux Privilege Escalation: Enumeration](https://tryhackme.com/room/linprivenum) | 🟦 THM | Linux basics + 3.4 | How to inspect a system after initial access. | 1 h |
| 4.2 | [RootMe Room](https://tryhackme.com/room/rrootme) | 🟦 THM | 3.4 + 4.1 | **The most Root-Me-linked room:** file upload → reverse shell → SUID escalation. | 45 min |
| 4.3 | [Linux - Privilege Escalation](https://www.root-me.org/en/Challenges/System/Linux-Privilege-Escalation) | 🟥 RM | 4.1 | Root Me focuses on specific techniques (SUID, cron, sudo) you must discover yourself. | 1 h |
| 4.4 | [Linux Privilege Escalation](https://tryhackme.com/room/linprivesc) | 🟦 THM | 4.2 | Deepen the enumeration-to-exploitation workflow. | 50 min |
| 4.5 | [Windows PrivEsc](https://tryhackme.com/room/windows10privesc) | 🟦 THM | Windows basics (from 0.2) | Windows privilege escalation (services, registry, permissions). | 1 h 15 min |
| 4.6 | [SUID - Search](https://www.root-me.org/en/Challenges/System/SUID-Search) | 🟥 RM | 4.3 | Find and exploit SUID binaries. | 30 min |
| 4.7 | [Sudo - Weak configuration](https://www.root-me.org/en/Challenges/System/Sudo-Weak-configuration) | 🟥 RM | 4.3 | Exploit weak sudo rules. | 30 min |
| 4.8 | [Cron - Weak permissions](https://www.root-me.org/en/Challenges/System/Cron-Weak-permissions) | 🟥 RM | 4.3 | Exploit cron jobs with weak permissions. | 30 min |

> ✅ **Transition criterion:** You escalate privileges on Linux and Windows using at least **three different techniques** without a walkthrough.

---

## 🧠 Phase 5 — Specialization Tracks

> **Goal:** After mastering the fundamentals, pick **one** track and finish it.

### ⚔️ Track A — Red Team / Penetration Tester

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? |
|:---:|:---|:---:|:---|:---|
| A.1 | [Jr Penetration Tester Path](https://tryhackme.com/path/outline/jrpenetrationtester) | 🟦 THM | Phases 1–4 complete | Full methodology: recon → exploitation → reporting. |
| A.2 | [Active Directory Basics](https://tryhackme.com/room/winadbasics) | 🟦 THM | A.1 | Understand AD before attacking it. |
| A.3 | [Attacktive Directory](https://tryhackme.com/room/attacktivedirectory) | 🟦 THM | A.2 | AS-REP, Kerberoasting, DCSync. |
| A.4 | [Realist - A bittersweet shellfony](https://www.root-me.org/en/Challenges/Realist/A-bittersweet-shellfony) | 🟥 RM | A.1 | Full realistic engagement. |
| A.5 | [Realist - Ultra-Upload](https://www.root-me.org/en/Challenges/Realist/Ultra-Upload) | 🟥 RM | A.1 | Realistic web exploitation. |

### 🛡️ Track B — Blue Team / SOC Analyst

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? |
|:---:|:---|:---:|:---|:---|
| B.1 | [SOC Level 1 Path](https://tryhackme.com/path/outline/soclevel1) | 🟦 THM | Phases 1–3 complete | SOC fundamentals, triage, reporting. |
| B.2 | [Phishing Analysis Fundamentals](https://tryhackme.com/room/phishingemails1tryoe) | 🟦 THM | B.1 | Analyze real phishing emails. |
| B.3 | [Splunk: Basics](https://tryhackme.com/room/splunk101) | 🟦 THM | B.1 | SIEM analysis. |
| B.4 | [Forensics - Malware](https://www.root-me.org/en/Challenges/Forensic/Malware) | 🟥 RM | B.1 | Real forensic analysis. |
| B.5 | [Network - PCAP](https://www.root-me.org/en/Challenges/Network/PCAP) | 🟥 RM | 1.2 + B.1 | Packet analysis. |

### 🧩 Track C — Application Security Engineer

| # | Room / Challenge | Platform | 🔒 Prerequisite | 🎯 Why? |
|:---:|:---|:---:|:---|:---|
| C.1 | [Advanced SQL Injection](https://tryhackme.com/room/advancedsqlinjection) | 🟦 THM | 2.4 | Blind, time-based, filter bypasses. |
| C.2 | [SSRF](https://tryhackme.com/room/ssrfhr) | 🟦 THM | 1.2 + 3.11 | Reaching internal services. |
| C.3 | [SSTI](https://tryhackme.com/room/learnssti) | 🟦 THM | 1.2 + PHP/Python basics | Server-side template injection. |
| C.4 | [Web - Java - Serialization](https://www.root-me.org/en/Challenges/Web-Server/Java-Serialization) | 🟥 RM | C.1 | Java deserialization. |
| C.5 | [Web - PHP - Filters](https://www.root-me.org/en/Challenges/Web-Server/PHP-Filters) | 🟥 RM | 3.11 | PHP filter exploitation. |

---

## 📅 Study Plans

### 16-Week Plan (Intensive — 20–25 h/week)

| Weeks | Phase | Focus |
|:---:|:---:|:---|
| 1 | 0 | Setup, platform, habits |
| 2–3 | 1 | HTML, HTTP, JS, Burp |
| 4 | 2 | XSS, SQLi |
| 5–6 | 3 | CSRF, File Upload, Command Injection, LFI/RFI |
| 7–8 | 4 | Linux & Windows PrivEsc |
| 9–12 | 5A | Jr Pentester Path (or chosen track) |
| 13–14 | 5B | AD + Realist challenges |
| 15–16 | Capstone | Full engagement + report |

### 9-Month Plan (Realistic — 8–10 h/week)

| Month | Phases |
|:---:|:---|
| 1 | 0 + 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |
| 5–6 | 5A (Red Team) |
| 7 | 5B (AD + Realist) |
| 8 | Blue Team cross-training |
| 9 | Capstone + portfolio |

---

## ✅ Phase Transition Criteria

Do not move on just because you finished the rooms. Move on when you meet the criteria.

| Transition | Practical criterion |
|:---|:---|
| 0 → 1 | You launch AttackBox/OpenVPN and solve `HTML - Source code` without help. |
| 1 → 2 | You intercept, understand, and modify a request in Burp unaided. |
| 2 → 3 | You solve XSS and SQLi on Root Me without copying a solution. |
| 3 → 4 | You obtain a shell on Root Me via file upload or command injection unaided. |
| 4 → 5 | You escalate privileges on Linux and Windows using 3+ different techniques. |
| 5 → Professional | Capstone + report + portfolio + 3 hard boxes. |

### Capstone Project

Pick one target (medium/hard) and run the full lifecycle:

1. **Scoping** — define scope and authorization.
2. **Recon** — passive and active with documentation.
3. **Enumeration** — every port, service, path.
4. **Exploitation** — initial access with documented steps.
5. **Privilege Escalation** — root/SYSTEM.
6. **Post-Exploitation** — what could you reach?
7. **Reporting** — professional report with severity, evidence, remediation.
8. **Retest** — verify the fix.

**Suggested targets:** `RootMe`, `Blog`, `Marketplace`, `HackNote`, `UltraTech`, `VulnNet`.

---

## 🏆 Golden Rules

1. **Never skip a prerequisite.** If the table says "JavaScript required," finish JavaScript first.
2. **Try for 30–60 minutes before looking at a walkthrough.** The struggle is the learning.
3. **Take notes for every room.** What worked, what failed, the lesson learned.
4. **Do not copy solutions.** If you can't explain it, you didn't learn it.
5. **Revisit hard rooms a week later.** Repetition is what makes a skill stick.
6. **Spend 30% of your time on defense**, even if your goal is red team.
7. **Document everything.** A portfolio of solved challenges is worth more than a certificate.

---

## 📊 Progress Tracker

Copy this checklist into your repo and check items off as you go.

```markdown
### Phase 0 — Setup
- [ ] 0.1 How to use TryHackMe
- [ ] 0.2 Pre Security Path
- [ ] 0.3 HTML - Source code (RM)
- [ ] 0.4 OpenVPN

### Phase 1 — Web Foundations
- [ ] 1.1 How Websites Work
- [ ] 1.2 HTTP in Detail
- [ ] 1.3 JavaScript Basics
- [ ] 1.4 Javascript - Authentication (RM)
- [ ] 1.5 Javascript - Obfuscation 1 (RM)
- [ ] 1.6 HTML - From the outside (RM)
- [ ] 1.7 HTTP - IP restrict access (RM)
- [ ] 1.8 HTTP - User-agent (RM)
- [ ] 1.9 Burp Suite: The Basics

### Phase 2 — First Vulnerabilities
- [ ] 2.1 Intro to XSS
- [ ] 2.2 XSS - Reflected (RM)
- [ ] 2.3 XSS - Stored 1 (RM)
- [ ] 2.4 SQL Injection Introduction
- [ ] 2.5 SQL injection - Authentication (RM)
- [ ] 2.6 SQL injection - String (RM)
- [ ] 2.7 SQL injection - Numeric (RM)

### Phase 3 — Advanced Web
- [ ] 3.1 CSRF Introduction
- [ ] 3.2 CSRF - 0 protection (RM)
- [ ] 3.3 CSRF - token bypass (RM)
- [ ] 3.4 File Upload Vulnerabilities
- [ ] 3.5 File upload - Double extensions (RM)
- [ ] 3.6 File upload - MIME type (RM)
- [ ] 3.7 File upload - Null byte (RM)
- [ ] 3.8 Command Injection
- [ ] 3.9 Command injection - Basic (RM)
- [ ] 3.10 Command injection - Blind (RM)
- [ ] 3.11 LFI (RM)
- [ ] 3.12 LFI - Journey through files (RM)
- [ ] 3.13 RFI (RM)
- [ ] 3.14 Backup files (RM)
- [ ] 3.15 Weak password (RM)

### Phase 4 — PrivEsc
- [ ] 4.1 Linux PrivEsc: Enumeration
- [ ] 4.2 RootMe Room
- [ ] 4.3 Linux - PrivEsc (RM)
- [ ] 4.4 Linux PrivEsc
- [ ] 4.5 Windows PrivEsc
- [ ] 4.6 SUID - Search (RM)
- [ ] 4.7 Sudo - Weak configuration (RM)
- [ ] 4.8 Cron - Weak permissions (RM)

### Phase 5 — Specialization
- [ ] Track chosen: ☐ Red ☐ Blue ☐ AppSec
- [ ] Track completed
- [ ] Capstone done
- [ ] Report written
- [ ] Portfolio published
