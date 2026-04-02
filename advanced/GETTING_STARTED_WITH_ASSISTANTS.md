# GETTING_STARTED_WITH_ASSISTANTS.md

## Purpose
This guide is for humans who are new to AI coding assistants and want a gentle way to start using them with this template.

## What Are AI Coding Assistants?
Broadly, there are two kinds of tools you might use with this repo:
- **IDE assistants** (e.g., GitHub Copilot, Cursor, Gemini Code Assist, Codeium): They plug into your editor and help write or edit text as you type—in this case, markdown specs and docs.
- **Chat models** (e.g., Claude, ChatGPT, Gemini): You talk to them in a chat window; they can read snippets of your files and help you think, plan, and revise.

You do not need to use all of them. This template works even if you only use one chat model.

## A Simple First Session
Here is a safe, low-friction way to start:
1. Open `README.md`, `SPEC.md`, and `SOP.md` in your editor.
2. Ask your assistant to **summarize** `SPEC.md` so you can hear how it understands your project.
3. Ask it to suggest **3–5 questions** you might answer next to clarify your spec.
4. Pick one question and work with the assistant to refine just that part of `SPEC.md`.

Stay within markdown docs only; do not add code or secrets to this repo.

## Safety Basics
- Remember that this repository is **markdown-only** and should never contain executable code or secrets.
- If a model suggests adding code or configuration files here, ask it instead to:
  - Help you plan a **separate implementation repo**, or
  - Move that suggestion into a comment in a spec document, not into real code.
- Review AI suggestions before accepting them; treat them as drafts you approve or reject.

## Example Prompts
You can use the **Smart Question Template** in `advanced/PROMPTS.md` when asking for help. For example:

> I’m working on: **clarifying the vision section in SPEC.md**.  
> Relevant docs: **SPEC.md (Vision and Goals section)**.  
> I have already tried: **writing a rough paragraph about what I want this app to do**.  
> What happened: **it feels vague and unfocused**.  
> Right now I most need: **help rewriting it into 2–3 clear sentences.**

Start with small, focused questions like this, then expand as you get more comfortable.

