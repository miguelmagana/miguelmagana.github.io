---
layout: page
title: ShellShocker
label: // portfolio
subtitle: AI-powered offensive security platform.
permalink: /shocker/
---

ShellShocker (5H3LL5H0CK3R) is a fully offline, production-grade AI orchestration system built for bug hunting and offensive security testing. Built from scratch in C# / .NET 10.

<a href="https://github.com/miguelmagana/5H3LL5H0CK3R" target="_blank" rel="noopener" class="btn">GitHub →</a>

---

## What It Does

ShellShocker coordinates AI-driven security testing against external targets through a hardened local inference stack. No cloud APIs. No external dependencies. Runs entirely offline on private networks.

The platform hosts three AI entities — each with a distinct role in the security testing pipeline:

<div class="card-grid">
  <div class="card">
    <p class="card-label">orchestrator</p>
    <h3>Ka0s</h3>
    <p>Architect and operator AI. Coordinates the testing pipeline, manages entity sessions, and is the only entity authorized to invoke the payload generation module.</p>
  </div>
  <div class="card">
    <p class="card-label">senpai</p>
    <h3>8l4d3</h3>
    <p>Elite hacker identity. Critiques findings, scores results, and trains BugB4ng3r through the AI pipeline.</p>
  </div>
  <div class="card">
    <p class="card-label">kohai</p>
    <h3>BugB4ng3r</h3>
    <p>Bug hunter identity. Executes security testing against external targets, invokes tool plugins, and learns from 8l4d3's critique.</p>
  </div>
</div>

---

## Architecture

```
WPF War Room UI  ─┐
Blazor Web UI    ─┤──→  gRPC Core.API  ──→  AI Engine (Mistral 7B local)
CLI (Go)         ─┘         │                    │
                            │              Qdrant vector memory
                            ↓
                     Tool Plugin Layer (ZeroBrain)
                            │
                    External target / scan output
                            │
                       LiteDB storage
```

**The rule:** C# builds the hammers (tool plugin wrappers). AI entities decide when to pick them up and how to use them. No security decision logic is compiled into C#.

---

## Tech Stack

<div class="tag-list">
  <span class="tag">.NET 10</span>
  <span class="tag">C#</span>
  <span class="tag">WPF + MVVM</span>
  <span class="tag">Blazor Server</span>
  <span class="tag">gRPC / grpc-dotnet</span>
  <span class="tag">Protocol Buffers</span>
  <span class="tag">LLamaSharp</span>
  <span class="tag">Mistral 7B GGUF</span>
  <span class="tag">Qdrant</span>
  <span class="tag">LiteDB</span>
  <span class="tag">Go (CLI)</span>
  <span class="tag">Nim (payload module)</span>
  <span class="tag">Python (recon)</span>
  <span class="tag">Clean Architecture</span>
  <span class="tag">xUnit + SpecFlow</span>
</div>

---

## Module Map

| Module | Language | Purpose |
|---|---|---|
| ShellShocker.AI | C# | Ka0s inference engine — LLamaSharp + Mistral 7B |
| ShellShocker.UI | C# / WPF | War room interface |
| ShellShocker.Web | C# / Blazor | Web interface |
| ShellShocker.Core | C# | Domain models, interfaces |
| ZeroBrain | C# | Tool plugin execution (IToolPlugin wrappers) |
| Skunkworks | Python | Passive recon and OSINT |
| Kitsune | Nim | Payload and evasion module (Ka0s authorized only) |
| OmniOps | — | Campaign orchestration |
| CLI-Cowboy | Go | Terminal interface |

---

## Current Status

The platform is in active development. The current milestone is **MVK (Minimum Viable Ka0s Conversation)** — the moment Ka0s receives a prompt and responds through the full gRPC pipeline to the UI. Ka0s must speak before any security feature is wired.

Build order: gRPC Core.API → MVK → Entity isolation → Qdrant RAG → tool plugins wired through Core.API.
