# CONTEXT_TRANSFER.md

Copy this file to **`CONTEXT_TRANSFER.md`** after you clone or fork (see root `.gitignore`). **`CONTEXT_TRANSFER.md` is not committed** so each session’s handoff stays local unless you choose to share it another way.

 **Purpose**: Temporary context handoff between AI models and devices.  
 This file is ephemeral — overwrite it each session. Do not commit private data.

## Named handoff files (`CONTEXT_TRANSFER_FROM_*`)

When an assistant **generates** a handoff for you, you can ask for an explicit filename so you know **which model and platform** produced it:

**Pattern:** `CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md`

Use short, consistent tokens (uppercase with underscores), for example:

- `CONTEXT_TRANSFER_FROM_CLAUDE_MOBILE.md`
- `CONTEXT_TRANSFER_FROM_CURSOR_DESKTOP.md`
- `CONTEXT_TRANSFER_FROM_CHATGPT_WEB.md`

**Workflow:**

1. Keep **`CONTEXT_TRANSFER.md`** as the single **canonical** copy you overwrite when you want one “current handoff” for the next session.
2. Use **`CONTEXT_TRANSFER_FROM_*`** when you want **provenance** (parallel mobile vs desktop notes) or before you merge into `CONTEXT_TRANSFER.md`.
3. In this template, **`CONTEXT_TRANSFER_FROM_*.md` is gitignored** by default so those drafts stay off the remote.

**Prompt snippet for models:** “Write the handoff to a new file named `CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md` using the same section structure as `CONTEXT_TRANSFER.md`.”

---

## Current Focus
<!-- One sentence: what were you actively working on? -->
Example: Finalizing the shape of SPEC.md required fields.

## Decisions Made This Session
<!-- Capture settled choices so the next model doesn't re-litigate them. -->
[ ] Example: Chose X over Y because Z.

## Open Questions / Blockers
<!-- What needs a decision or discussion next? -->
[ ] Example: Should AGENTS.md define verbosity per-tool or globally?

## Items to Plan / Discuss
<!-- Agenda for the next session, especially useful for voice/mobile. -->
[ ] Example: Walk through SOP.md mobile workflow section.

## How to Resume
<!-- What to say/paste to orient the next model quickly. -->
1. Share or link this file.
2. Say: "Continue work on [repo name]. See CONTEXT_TRANSFER.md for current state."
3. Optionally share CONTEXT.md for full project background.

---
Last updated: [date] by [model or human]
