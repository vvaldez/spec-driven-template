# PROMPTS.md

## Purpose
Collect reusable prompt patterns for common tasks in this template, so you do not have to invent them from scratch each time.

## Planning Prompts
Examples for defining or refining specs and workflows.

### Smart Question Template (Goal → Tried → Result → Ask)
Use this pattern when asking an assistant for help:

> I’m working on: **[brief goal or task]**.  
> Relevant docs: **[files/sections you’ve looked at]**.  
> I have already tried: **[what you did or thought about]**.  
> What happened: **[what you observed / why it’s not good enough]**.  
> Right now I most need: **[explanation / options / critique / next step]**.

You can paste and fill this in when asking questions to keep them focused and productive.

## Refactoring and Restructuring Prompts
Examples for reorganizing sections, splitting documents, or simplifying text.

## Debugging and Risk Analysis Prompts
Examples for stress-testing plans, uncovering risks, or clarifying assumptions.

## Context-Sync and Handoff Prompts
Examples for moving context between mobile and desktop, or between different assistants, while staying anchored to this repository.

### Handoff file with provenance (`CONTEXT_TRANSFER_FROM_*`)

> Fill in a handoff using the same section headings as root **`CONTEXT_TRANSFER.md`** (Current Focus, Decisions, Open Questions, Items to Plan, How to Resume). Save it as **`CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md`** — for this session use **`CONTEXT_TRANSFER_FROM_[MODEL]_[PLATFORM].md`** (replace with short tokens, e.g. CLAUDE_MOBILE, CURSOR_DESKTOP). Do not include secrets or private data.

