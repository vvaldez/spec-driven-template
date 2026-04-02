# PERSONAS.md

 **Purpose**: Describes typical human users of this template and maps each to a recommended starting path.  
 Use this file to find yourself, then follow your recommended reading list.

-----

## How to Use This File

Skim the personas below. Pick the one that fits best — or mix two if you sit between them. Then follow the suggested path. You do not need to read everything; the paths are designed to get you productive with the minimum number of files.

-----

## Persona 1: The Curious Non-Developer

**Who you are**: You are not a programmer. You may have used ChatGPT, Claude, or similar tools to help you write, plan, or brainstorm — but you have never written code professionally and do not intend to start now. You have an idea for something you want to build or automate and you are exploring whether AI tools can help you get there.

**Your goals**:

Understand what this template is and whether it applies to you.
Start describing your idea in plain language.
Figure out what to ask an AI assistant to do next.

**Your recommended path**:

1. README.md — Read the “What This Is” and “Who This Is For” sections.
1. AGENTS.md — Skim the “Read This First” section so you understand what the AI can and cannot do here.
1. SPEC.md — Start filling in “Vision and Goals” in plain language. Don’t worry about the rest yet.
1. advanced/GETTING_STARTED_WITH_ASSISTANTS.md — A gentle introduction to AI tools and how to use them with this template.

**What to skip for now**: Everything else. Come back when you feel stuck or curious.

-----

## Persona 2: The Developer, AI Novice

**Who you are**: You are comfortable writing code and have worked on real projects. You are newer to AI-assisted workflows — you may have used GitHub Copilot for autocomplete but have not built a multi-model planning workflow before. You want structure and want to understand the “why” before diving in.

**Your goals**:

Understand the spec-driven approach and how it differs from jumping straight to code.
Set up a clean planning workflow before writing implementation code.
Learn how to coordinate multiple AI tools across desktop and mobile.

**Your recommended path**:

1. README.md — Full read.
1. AGENTS.md — Full read, especially the “Guidelines by Agent Type” section.
1. SPEC.md — Fill it out before opening your IDE.
1. SOP.md — Read the workflow conventions before starting daily work.
1. SECURITY.md — Understand the planning vs. implementation repo split.
1. advanced/ — Explore when you want more structure (architecture, decisions, risks).

**What to skip for now**: HUMAN.md and CONTEXT.md — fill those in as you go.

-----

## Persona 3: The AI-Native Non-Developer

**Who you are**: You are a power user of AI tools — you prompt well, you know how to get results from Claude, ChatGPT, or Gemini, and you may already have a multi-model workflow. You are not a programmer but you are technically confident. You want to use this template as a structured way to drive AI assistants toward a real outcome.

**Your goals**:

Use this template as a coordination layer across multiple AI tools and devices.
Keep planning separate from implementation so you do not accidentally create a mess.
Get AI assistants to do more consistent, predictable work.

**Your recommended path**:

1. AGENTS.md — This is your file. Read it fully; it describes how to set expectations for every assistant you use.
1. README.md — Skim for structure.
1. SPEC.md — Fill in your idea; you already know how to prompt, so this should feel natural.
1. SOP.md — Review the multi-device and mobile workflow sections.
1. CONTEXT.md — Start using this immediately as your live project snapshot.
1. advanced/PROMPTS.md — Useful prompt patterns for driving AI assistants with this template.

-----

## Persona 4: The Full-Stack AI Developer

**Who you are**: You write code daily, you have used multiple AI coding assistants, and you have probably already built a multi-model workflow of your own. You are picking up this template because you want a clean, portable planning layer that you can fork and adapt quickly.

**Your goals**:

Evaluate the template structure quickly.
Adapt it to your existing workflow with minimal friction.
Understand the opinions baked in and decide which ones to keep.

**Your recommended path**:

1. README.md — Skim for structure and opinions.
1. AGENTS.md — Note the tool-agnostic contract pattern; adapt for your tools.
1. SPEC.md and SOP.md — Review the templates; modify to fit your standards.
1. advanced/ — Browse freely; treat as a menu of optional add-ons.
1. advanced/ORIGIN_STORY.md — Useful if you want to understand the design decisions behind this template.

**What to skip**: GETTING_STARTED_WITH_ASSISTANTS.md — you don’t need it.

-----

## Progressive Disclosure Map

|Persona             |Root Files                |Advanced Files                |Skip           |
|--------------------|--------------------------|------------------------------|---------------|
|Curious Non-Dev     |README, AGENTS, SPEC      |GETTING_STARTED               |Everything else|
|Developer, AI Novice|All root files            |Architecture, Decisions, Risks|—              |
|AI-Native Non-Dev   |AGENTS, SPEC, SOP, CONTEXT|PROMPTS                       |GETTING_STARTED|
|Full-Stack AI Dev   |README, AGENTS, SPEC, SOP |All advanced/                 |GETTING_STARTED|

-----

## A Note on Personas and Reality

You may not fit neatly into one box. That is fine. These personas are starting points, not labels. If you are between Persona 1 and Persona 2, start with Persona 1’s path and add Persona 2’s files when you feel ready. The goal is to reduce overwhelm, not to categorize you permanently.

-----

**Implemented elsewhere:** `README.md` (first-session prompt and default Persona 1) and `AGENTS.md` (persona-aware disclosure) connect these personas to assistant behavior. You can still extend this file with more detail or new personas over time.