# Tether — Demo

*How to watch the gate work. No code to install, no internals to read.*

## The live console

The public gate console is live at:

**https://gate-console-app.pages.dev**

It shows the gate's decisions — PERMIT and HOLD — on synthetic data. Nothing in it is a real customer system, and nothing you do there touches a real action.

## What to look for

1. An action with a valid permit executes.
2. The same action with no permit holds.
3. The same action with a permit for a *different* action holds.
4. A permit used twice holds the second time.

That is the whole demo: the gate does not care who the agent is or how reasonable the action sounds. It cares whether a signed permit exists for that exact action, right now.

## A scoped pilot

The console is a window, not the product. A pilot puts the real gate in front of one of your workflows, with a permit check on every action in it.

To scope a pilot, contact hello@shaethonai.com. One scoped workflow, your hardest agent actions.

## What is not here

There is no code in this repository, no SDK, and no way to run Tether yourself from these files. That is deliberate. Tether is sold as a pilot and a license, not as code to copy.
