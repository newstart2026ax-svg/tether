# Tether — Spec

*What Tether guarantees. No implementation details, no code, no internals.*

## The rule

**No permit, no execution.**

Every action an agent wants to take through a Tether-gated system needs a signed permit for that exact action, at that moment. Without it, the action holds. There is no default allow.

## The guarantees

1. **One permit, one action.** A permit covers one exact action, with its exact arguments. It cannot be stretched to a different action, a different target, or a different amount.
2. **Fresh every time.** Every action needs a fresh permit. A permit from a previous action does not carry over, and a workflow is not a blanket permit.
3. **Checked outside the agent.** The check happens at the gate, not inside the agent. An agent that is compromised, manipulated, or prompt-injected cannot check itself through.
4. **Hold, don't guess.** If anything about the permit does not match — wrong action, wrong arguments, expired, already used — the action holds. Tether fails closed.
5. **Evidence for every decision.** Every permit check leaves a signed, tamper-evident record: what was asked, what was permitted or held, and when.

## The loop

Tether works with two companion layers, in this order:

**AirGap → Tether → Pulpo → Tether → AirGap**

- **AirGap** inspects what the agent carries, strips it down, and rebuilds it clean. Nothing tampered enters to call the gate.
- **Tether** permits the action — or holds it.
- **Pulpo** organizes the workflow into clean, repeatable jobs. Every action in the workflow still comes back to Tether for a fresh permit.

Hold lives only at the Tether permit check.

## What a permit is (in plain language)

A permit is a signed statement that a specific agent may perform a specific action, with specific arguments, within a specific window. It is issued by a human-held authority, not by the agent itself. It is used once.

This document deliberately does not specify the permit's format, fields, signing method, or storage. Those are the internals, and they are not for sale in this repository — they are what a pilot and a license buy.

## What Tether does not do

- It does not stop direct hacker attacks in general. It stops a compromised or manipulated agent from executing outside its assignment, through Tether-gated systems.
- It does not judge whether an action is wise or ethical. It enforces whether it was permitted.
- It does not replace identity, access control, or monitoring. It is the execution check those systems do not provide.

## Status

Tether is live at gate.shaethonai.com and pilot-ready. It has been independently tested by an outside competitor: 39 scenarios, zero unauthorized executions, 36 clean holds, 3 flags found and fixed the next day. No paid pilot has been signed yet.

## Contact

hello@shaethonai.com — Founder, SHAETHON AI
