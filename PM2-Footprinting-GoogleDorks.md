# PM2 — Footprinting & Reconnaissance with GHDB (Google Hacking Database)

**Method:** Passive reconnaissance using Google Dorks
**Source:** https://www.exploit-db.com/google-hacking-database

---

## Background

Google Dorks are specialized search queries using operators like `site:`, `filetype:`, `inurl:`, `intitle:`, and `intext:` to find publicly indexed information that a website has unintentionally exposed. This is passive recon — no direct contact is made with the target, only Google's own index is queried.

---

## Task 1: Finding Publicly Exposed/Indexed Resources (Live Example)

**Dorks Used:**
intitle:“webcamXP” inurl:8080

**Screenshots:**
👉 **<img width="959" height="402" alt="1 (109 )" src="https://github.com/user-attachments/assets/e28b7f73-3666-4aec-aa5d-293188d91e69" />
**
👉 **<img width="959" height="409" alt="3 (72 199 )" src="https://github.com/user-attachments/assets/68a3b69f-df7c-4abc-95dc-8b134baabd73" />
**
👉 **<img width="957" height="409" alt="4 (85 93 )" src="https://github.com/user-attachments/assets/f0df8e9b-65c0-4e67-9834-58130b439064" />
**

**Findings Table:**

| # | Link | Dork Used | Username/Password |
|---|---|---|---|
| 1 | (http://109.233.191.130:8080/) | intitle:"webcamXP" inurl:8080 | N/A |
| 2 | (http://72.199.200.5:8080/home.html) | intitle:"webcamXP" inurl:8080 | N/A |
| 3 | (http://85.93.53.175:8080/multi.html) | intitle:"webcamXP" inurl:8080 | N/A |

**Observation:**
Most results required authentication or were no longer accessible, confirming that owners had secured exposed devices over time. In line with ethical OSINT practice, no live feeds were accessed that could belong to real individuals.

---

## Task 2: Finding Publicly Indexed Mathematics eBooks (Open Directories)

**Dorks Used:**
intitle:index.of “mathematics” filetype:pdf
intitle:index.of “MathBooks”
site:archive.org intitle:index.of mathematics filetype:pdf

**Screenshots:**
👉 **<img width="950" height="440" alt="Annals of math" src="https://github.com/user-attachments/assets/10427703-5159-42c0-8020-205bf5a9e226" />
**
👉 **<img width="957" height="415" alt="Fundamentals of math" src="https://github.com/user-attachments/assets/2f41ba97-dd57-493b-9db5-191cac588d36" />
**

**Findings Table:**

| # | Link | Dork Used | Username/Password |
|---|---|---|---|
| 1 | https://archive.org/details/cnx-org-col10615 | site:archive.org intitle:index.of mathematics filetype:pdf | N/A — open directory |
| 2 | https://webhomes.maths.ed.ac.uk/~v1ranick/papers/as4.pdf | intitle:index.of "mathematics" filetype:pdf | N/A — open directory |

---

## How Attackers Use This Information

- **GHDB dorks** allow attackers to find exposed devices, backup files, login panels, or sensitive documents without ever sending a direct request to the target — Google has already crawled and indexed it.
- Because no packets are sent to the target itself, this form of recon is **extremely hard to detect**.
- Organizations can defend against this by periodically dorking their own domain and removing anything sensitive from Google's index via Search Console.
