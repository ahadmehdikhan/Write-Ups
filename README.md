# PortSwigger Web Academy — Server-Side Vulnerabilities (Writeups)
**Hands-on lab writeups, PoC scripts, and remediation notes.**  
Completed: 2025-10-01

**Scope:** SSRF, insecure deserialization, path traversal, file upload flaws, OS command injection, SQL injection, broken access controls, authentication weaknesses, and related server-side issues.

This repo is structured to be **HR-friendly for quick skim** and **technically actionable for reviewers**. PoCs are lab-only and safe to run only in controlled environments.

---

## Quick TL;DR (for recruiters)
Entry-level vulnerability tester — documented and reproduced server-side vulnerabilities using PortSwigger Web Academy labs. Created concise writeups, PoC scripts (Python), and developer-focused mitigations.

---

## Repo structure

portswigger-server-side/
├─ README.md
├─ summary.md
├─ labs/
│ ├─ 01-ssrf/
│ │ ├─ README.md
│ │ ├─ poc.py
│ │ └─ screenshots/
│ ├─ 02-deserialization/
│ ├─ 03-path-traversal/
│ ├─ 04-file-upload/
│ ├─ 05-os-command-injection/
│ ├─ 06-sql-injection/
│ ├─ 07-authentication/
│ └─ 08-access-control/
├─ tools/
├─ images/
├─ summary.md
└─ LICENSE



---

## How to read this repo
1. `summary.md` — one-page index with outcomes.  
2. `labs/<lab>/README.md` — full writeup for each lab (objective, environment, step-by-step reproduction, PoC, remediation).  
3. `labs/<lab>/poc.py` — minimal PoC scripts (only for safe lab use). Each script starts with usage comments and warnings.

---

## Example lab README
### Lab: <Name> — PortSwigger Web Academy — Server-Side Vulnerability  
**Solved on:** YYYY-MM-DD  
**Difficulty:** Beginner / Intermediate / Advanced  
**Tags:** <SSRF | Deserialization | Path Traversal | File Upload | OS Command Injection | SQLi | Auth | Access Control>

#### Objective
Short description: what the lab demonstrates and the impact if exploited.

#### Environment
- Browser: BURP Browser (chromium) 
- Tools: Burp Suite (Community)
- Lab host:PortSwigger lab

#### Steps to reproduce (concise & numbered)
1. Request: `POST /upload` with `filename=...`  
2. Intercept with Burp → modify parameter X → observe response Y  
3. Trigger final payload to achieve Z

*(Include exact request/response snippets, redacting any sensitive/session tokens.)*

#### PoC
`poc.py` — usage: `python3 poc.py --target http://localhost:8080 --payload payload.txt`  
Comments inside script explain the flow. **WARNING: Lab use only.**

#### Result / Impact
What an attacker can do (file read, remote code execution, internal network access, DB exfiltration).

#### Mitigation
Concrete developer guidance (allowlist, input validation, principle of least privilege, disable dangerous functions, safe deserialization libraries, content-type checks, multi-factor auth, rate limit authentication endpoints).

#### Notes / Lessons learned
Two lines about personal learning and next steps.

---

## Ethical notice
All PoCs and testing were performed on PortSwigger labs. Do not run PoCs against systems you do not own or have explicit permission to test.

---

