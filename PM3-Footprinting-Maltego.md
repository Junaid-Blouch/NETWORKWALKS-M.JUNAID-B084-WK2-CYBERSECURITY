# PM2 — Graphical OSINT & Link Analysis with Maltego

**Target:** `networkwalks.com` (Authorized Lab Environment)  
**Tool Used:** Maltego Graph (Desktop) v4.14.0 — Community / Standard Transforms  

---

## Objective
Conduct Open-Source Intelligence (OSINT) and visual link analysis using **Maltego** to map domain infrastructure, discover associated email addresses, extract metadata from public documents, and correlate entities from a SOC Analyst and Threat Intelligence perspective.

---

## Task 1: Maltego Environment & Transform Hub Setup

**Action Performed:**  
Launched Maltego Graph Desktop (`v4.14.0`) and verified active Transform Hub integrations (238 installed transforms across Recon, Infrastructure, Threat Intelligence, and Breach categories).

**Screenshot:**  
👉 **<img width="959" height="491" alt="Maltego home" src="https://github.com/user-attachments/assets/20702ef5-461b-48b3-9153-9317936171c5" />
**

**SOC Analyst Note:**  
Before initiating an investigation, confirming active data hubs ensures that domain, DNS, and metadata transforms can query public intelligence repositories accurately without API failure.

---

## Task 2: Domain Entity Mapping & Email Discovery (Transforms)

**Action Performed:**  
1. Dragged a **Domain** entity from the Entity Palette onto a new investigation graph and set the value to `networkwalks.com`.
2. Executed **Email Address Transforms** against the domain entity to uncover publicly indexed contact points.

**Screenshot:**  
👉 **<img width="959" height="500" alt="Maltego domain search" src="https://github.com/user-attachments/assets/ce137d2e-dc3c-4985-828c-3f0412f0b09a" />
**

**Findings:**  
- **Target Domain:** `networkwalks.com`
- **Discovered Entity:** `info@networkwalks.com` (Public administrative/contact email address)

---

## Task 3: Automated Footprint & Metadata Extraction (Machines)

**Action Performed:**  
Executed an automated **Maltego Machine** (Footprint / Metadata parsing pipeline) on the target domain to enumerate linked documents, individuals, phrases, and network relationships.

**Screenshot:**  
👉 **<img width="959" height="504" alt="Maltego machine feature" src="https://github.com/user-attachments/assets/d211a7d5-a5c3-4ea6-b383-fde4943a8a72" />
**

**Findings & Graph Metrics:**  
- **Total Entities Mapped:** `55 Entities` (Domains, Documents, Persons, Phrases, and Email Addresses)
- **Total Relationships:** `137 Links`
- **Transform Activity:** Parsed metadata from publicly hosted documents (`Parse meta information` utility transform completed), extracting author names, software strings, and contextual keywords.

---

## Security & SOC Analyst Takeaways

### How Attackers Leverage This Information
- **Phishing & Social Engineering:** Discovered email addresses (`info@networkwalks.com`) and extracted employee names from document metadata allow threat actors to craft convincing spear-phishing or Business Email Compromise (BEC) lures.
- **Metadata Leakage:** Public PDFs and Office documents often retain internal usernames, software versions, and file paths in their metadata, aiding attacker reconnaissance.

### Defensive / Blue Team Mitigations
- **Metadata Scrubbing:** Strip EXIF and document properties from all files before publishing them to public web servers.
- **Email Hardening:** Enforce strict **SPF**, **DKIM**, and **DMARC (`p=reject`)** policies on discovered corporate domains to prevent spoofing.
- **Attack Surface Monitoring:** Regularly run OSINT link analysis against organization domains to identify unauthorized public exposures.
