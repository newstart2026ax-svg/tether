# Tether — the deterministic permit gate for AI agents

**No permit, no execution.**

Tether is built by SHAETHON AI. It is the gate that sits between an AI agent and the action it wants to take. An agent proposes an action. Tether checks for a signed permit for that exact action, with those exact arguments, right now. Permit present and valid, the action executes. No permit, it holds.

This repository contains **no code and no internals**. It exists so a buyer, a CISO, or an investor can understand what Tether is, what it guarantees, and how to see it work — without ever seeing how it works inside.

- [The spec](SPEC.md) — what Tether guarantees, in plain language
- [The demo](DEMO.md) — how to watch the gate work, live
- [shaethonai.com](https://shaethonai.com) — SHAETHON AI
- [Public console](https://gate-console-app.pages.dev) — the live gate console
- Contact: hello@shaethonai.com

## What Tether is

AI agents act now. They move money, touch accounts, change records, and call other systems. The tools that watch them mostly watch *after* the fact — logs, alerts, rollbacks.

Tether checks *before* the fact. One permit, one exact action, once. A fresh permit every time. Nothing executes without one.

## What Tether is not

- Not a scanner, not an antivirus, not a malware filter
- Not an ethics engine — it does not decide what is right, it enforces what was permitted
- Not a general hacker defense — it stops a compromised or manipulated agent from executing outside its assignment, through Tether-gated systems

## Deployments

Tether is a gate. It deploys into the places agents act:

- **MedGate** — healthcare
- **BankGate / WireGate** — financial services
- **LawGate / CourtGate** — legal
- **DefenseGate** — defense systems

Each deployment is the same gate, scoped to that world's workflows.

## Pilots

Tether is pilot-ready. A pilot is one scoped workflow, with a signed permit check on every action in it. Contact hello@shaethonai.com to scope one.

## Rights

All content in this repository is © SHAETHON AI, all rights reserved. No license is granted to copy, reuse, or reproduce any of it. Reading it is not permission to build it.
