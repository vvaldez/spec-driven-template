# ORIGIN_STORY.md

## ForkIt in One Paragraph
ForkIt (“Fork it, I'll cook it myself”) is a DoorDash-inspired app that flips the delivery model: instead of paying fees for takeout, you use a familiar, slick UI to discover recipes, coordinate meals with family, and generate grocery lists that save money. It leans on three pillars from the start: DoorDash-style UX, an explicit anti-fee/savings focus, and recipe discovery and sharing as a collaborative activity.

## From Idea to Spec-Driven Project
Before (and alongside) building ForkIt, the project was grounded in written specs. `REQUIREMENTS.md` captures pillars, personas, constraints, and a feature breakdown that made it easier to reason about the product without getting lost in code details. This written-first habit is what naturally led toward a spec-driven style of development, even before naming it that way. Over time, that document naturally wanted to become a more general `SPEC.md`, while additional files like `SOP.md` and `MILESTONES.md` emerged to capture process and progress.

## Living the Milestones
`MILESTONES.md` documents how ForkIt grew in stages: popular recipe retrieval, a DoorDash-style mobile UI, cart and grocery list flows, group ordering, search and filter overhaul, the “What do you feel like?” questionnaire, savings dashboard, and the leftovers board. Each milestone ties back to requirements and pillars, making it easier to see why a change exists instead of treating it as an isolated commit. That milestone-driven story is part of what inspired having `MILESTONES.md` as an optional advanced doc in this template.

## Pain Points That Led to This Template
Building ForkIt with multiple tools and on different machines (a Mac at work for other projects, and a separate Windows gaming PC at home for ForkIt) surfaced recurring pain points: context loss between sessions, friction when switching devices, and the difficulty of keeping specs, milestones, and actual code in sync. The author deliberately kept work and home projects separate, but even with that separation it became clear that mixing “planning” and “implementation” in the same repo made it harder to safely invite AI tools into the process, especially when secrets and code lived next to high-level specs. Early experiments with provider-specific agent configs (such as `GEMINI.md`) also highlighted how fragile it can be when a workflow is tied too tightly to one tool’s quirks or quotas.

## Tool Hops and Agent Files
Along the way, the project touched several assistants: Gemini for early tasks, Claude Code for transformative refactors, Cursor for agentic coding, and Gemini Code Assist and Copilot within VS Code. At one point, an unrecoverable agent crash (a missing curly brace loop) and quota issues in Gemini pushed the workflow toward a more portable pattern: a `GEMINI.md` file that explained how to start the app, alongside `REQUIREMENTS.md`, `SOP.md`, and `MILESTONES.md` for the broader shape of the project. When switching to Cursor Pro, that provider-specific file was effectively generalized into `AGENTS.md`, and some of the original specs were restructured. That experience directly influenced this template’s preference for a single, tool-agnostic `AGENTS.md` plus reusable spec and process docs.

## From ForkIt to This Template
Those lessons motivated the design of this markdown-only, planning-first template. Instead of blending everything into one codebase, this repository is intentionally inert and focused on shared specs (`SPEC.md`), workflows (`SOP.md`), safety (`SECURITY.md`), and human context (`HUMAN.md`). The `.advanced/` directory reflects the same progression the author went through with ForkIt: starting simple and then gradually adding structure like milestones, decisions, risks, and personalized workflows once they became useful.

## Design Principles Encoded Here
Some of the key principles distilled from the ForkIt journey and captured in this template are:
- **Separate planning from implementation**: this repo never holds code or secrets; real apps live in their own implementation repos.
- **Specs and milestones as first-class citizens**: requirements and milestones deserve their own documents, not just commit messages.
- **Multi-model, multi-device friendly**: workflows should assume you may use different assistants on desktop and mobile, including voice, without losing the thread.
- **Progressive complexity**: start with a few core markdown files, then “unlock” advanced docs as needed rather than front-loading everything.

## How to Use This Origin Story
You do not need to know the details of ForkIt to use this template, but this origin story can spark ideas for your own projects. If you already have an app (or a half-built prototype), you can mirror this pattern: write down your pillars, personas, constraints, and features; capture milestones as you go; decide explicitly which parts of your workflow belong in a safe, markdown-only planning space and which belong in a separate implementation repo; and work with your agent of choice to bring your idea to life.

