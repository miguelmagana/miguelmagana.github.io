---
# miguelmagana.github.io — Agent Context

> Read this file at the start of every session on this repo.

## What This Is

Personal site for Miguel Magana — career hub, portfolio, and operator profile.
Lives at `miguelmagana.github.io`. Managed as a submodule of `life-os`.

## Operator Identity

```
Handle:    3l_p1r474 / The Finger Slinger
Company:   M Square LLC → msquarellc.net
Email:     m1k3.0xd@gmail.com
Location:  Hidden war room, back of the smoke shop
```

## Verified Background (from cv/Miguel_Magana_Master_Resume.docx)

**Career arc:** U.S. Navy (10 yrs) → Defense contractor (11 yrs) → ISP Network Engineer (current) → Offensive Security

### Experience Summary (skill-level — no employer names on site)
- **Navy (E1–E6, 10 years):** Classified systems, avionics, fiber-optic/RF circuits to component level,
  SCIF/physical security, led 11 personnel. Shipboard and test flight environments.
- **Defense contractor (11 years):** EO/IR sensor systems SME on defense programs, SCIF-adjacent
  protocols, Python/MATLAB automation for R&D test throughput, Scrum & Waterfall program leadership.
- **ISP/carrier network engineering (current):** Fiber network design, DWDM, MPLS, BGP, OSPF,
  Cisco IOS, Arista EOS, Calix, ADVA, incident response, carrier-grade uptime.

### Education & Certifications — VERIFIED ACCURATE
- B.S., Computer Networks & Cybersecurity — UMGC, 2022 (offensive security / red team focus)
- Certificate in Computer Networking — UMGC, 2022
- OSCP — **In Progress, Target: December 2026** (PWK/PEN-200 not yet started)

**CRITICAL:** Do NOT list PWK/PEN-200 as completed. It is NOT done.
No other industry certifications exist. Do not infer or add any.

### Technical Stack
- Offensive: Kali Linux, Metasploit, Nessus, OpenVAS, Burp Suite, Wireshark, OWASP ZAP, enum4linux
- Network: DWDM, MPLS, BGP, OSPF, fiber, Cisco IOS, Arista EOS, Calix, ADVA
- Programming: Python, Bash, C#, Go, Nim, PowerShell, SQL, JavaScript
- Frameworks: NIST 800-53, OWASP Top 10, CIS Controls, MITRE ATT&CK

## Purpose

This site is the personal brand layer — not the company layer (that's msquarellc.net).

Target audiences:
1. **Recruiters / hiring managers** — Network Security / Cybersecurity Engineer / Pentesting roles
2. **Bug bounty / security community** — portfolio + tool showcase
3. **Inbound from M Square** — bridge between personal and company

Target job titles: Network Security Engineer · Cybersecurity Engineer · Penetration Tester ·
Red Team Operator · Security Operations Engineer · Information Security Analyst ·
Vulnerability Assessment Analyst · Cloud Security Engineer · Systems Engineer (Defense/DoD)

## Stack Decision (TBD — awaiting m1k3 approval)

Recommendation: **Jekyll** — GitHub Pages native, zero build pipeline, markdown content,
operator aesthetic achievable via custom `_layouts` + CSS.
Upgrade path: Astro when/if the site outgrows it.

## Approved Site Structure

```
/           → Hero: "Operator." Handle, one-line arc, two CTAs
               [ShellShocker] [Hire Me]

/about      → Career arc as a story (not a job list)
               Navy → Defense → ISP → Offensive Security

/shocker    → ShellShocker deep-dive (centerpiece portfolio piece)
               Architecture, entity model (sanitized), tech stack, GitHub link

/skills     → Pentest competency cards → links to msquarellc.net writeups
               NOT a content dump — skill-area summaries that funnel to the business site

/roadmap    → UMGC BS + Certificate (2022) → OSCP (Dec 2026 active target)
               One horizontal timeline, no badge wall

/contact    → M Square LLC link · GitHub · Email
```

## Key Content Rules

1. **No employer names** — describe capabilities, not clients or employers
2. **ShellShocker is the centerpiece** — most applicants link to a todo app; this is an AI-powered
   offensive security platform (.NET 10 / C# / WPF / Blazor / gRPC / LLamaSharp / Qdrant)
3. **Pentest writeups live at msquarellc.net** — this site links there, never duplicates
4. **M Square LLC**: one-line mention + link only — no company content in personal repo
5. **OSCP = December 2026 target** — the one active milestone
6. **No fabricated certs** — if it's not in this CLAUDE.md, do not add it
7. **Aesthetic**: operator-coded — dark terminal feel, monospace, neon accents — NOT generic template

## Repo Commands

```bash
# Working from life-os root
cd miguelmagana.github.io

# Jekyll (once stack is confirmed):
# bundle exec jekyll serve   ← local preview
# git push origin main       ← GitHub Pages auto-deploys
```
