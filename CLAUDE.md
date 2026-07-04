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

## Purpose

This site is the personal brand layer — not the company layer (that's msquarellc.net).

Target audiences:
1. **Recruiters / hiring managers** — Network Security / Cybersecurity Engineer roles
2. **Bug bounty / security community** — portfolio + tool showcase
3. **Inbound from M Square** — bridge between personal and company

## Stack (TBD — awaiting m1k3 decision)

Options under consideration:
- Jekyll (GitHub Pages native, zero build pipeline)
- Astro (static-first, modern, Node.js ecosystem)
- Hugo (fast, minimal, Go-based)
- Plain HTML/CSS (full control, zero dependencies)

## Site Structure (approved direction)

```
/           → Operator profile / hero — dual-track identity (telecom → offensive security)
/portfolio  → ShellShocker showcase + pentest skill cards → links to msquarellc.net posts
/roadmap    → Cert roadmap — completed + OSCP December target
/contact    → Link to M Square LLC for business inquiries
```

## Key Content Rules

- Network engineering experience: **describe at skill/competency level**, not employer-specific
  (fiber ops, DWDM, topology automation, provisioning automation — capabilities, not clients)
- ShellShocker (5H3LL5H0CK3R): **lead asset** — AI-powered offensive security platform,
  .NET 10 / C# / WPF / Blazor / gRPC / LLamaSharp / Qdrant
- Pentest writeups live at msquarellc.net — this site links there, does NOT duplicate
- M Square LLC: one-line mention + link — do not pull company content into personal repo
- Job titles to position for: Network Security Engineer · Cybersecurity Engineer ·
  Penetration Tester · Red Team Operator · Security Operations Engineer ·
  Information Security Analyst · Vulnerability Assessment Analyst ·
  Cloud Security Engineer · Systems Engineer (Defense/DoD)

## Repo Commands

```bash
# Working from life-os root
cd miguelmagana.github.io

# Build (fill in once stack is decided)
# Deploy: git push origin main → GitHub Pages auto-deploys
```

## Agent Rules

1. No employer names — describe capabilities, not employers
2. ShellShocker is the centerpiece portfolio piece — treat it as such
3. Link out to msquarellc.net for pentest writeups — never duplicate
4. OSCP = December 2026 target milestone
5. Aesthetic: clean, technical, operator-coded — not generic resume template energy
