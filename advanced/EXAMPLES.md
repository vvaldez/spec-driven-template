# EXAMPLES.md

## Purpose
Show practical examples of how to use this template on a real or hypothetical project.

## Example: First-Time Setup (Software-Oriented)
A new user clones the template and wants a small web app.

1. Copy `CONTEXT.example.md` → `CONTEXT.md` and note today’s goal in one paragraph.
2. Read `AGENTS.md` (rules) and skim `SECURITY.md`.
3. In `SPEC.md`, fill **Vision and Goals** and **Personas / Users** for the app.
4. Add three items under **High-Level Feature List**, then expand one in **Feature Specifications** with acceptance criteria.
5. When ready for code, follow `README.md` → **Creating a Separate Implementation Repository**, complete the optional acknowledgment in `HUMAN.md` if they use it, then create the new repo and copy only the specs they need.

## Example: Non-Software Walkthrough — Short-Film Treatment
Same template, creative outcome: a 12-minute short film.

**Day 1 — Clone and frame the work**

- Copy context templates as in the software example.
- Read `README.md` “What This Is” and **Persona 1** path in `advanced/PERSONAS.md`.
- Open `SPEC.md` → **Vision and Goals**: logline, tone (e.g. bittersweet comedy), intended festival tier or audience.

**Day 2 — Structure as “features”**

- **High-Level Feature List**: e.g. Act 1 setup, midpoint reversal, climax, tag; casting constraints; one practical location rule.
- **Feature Specifications**: pick “Act 1” — problem (what the protagonist wants), proposed solution (how the draft establishes it), audience experience (what the viewer should feel by minute 4), acceptance criteria (“opening image echoes closing image,” “antagonist introduced by minute 3”).

**Day 3 — Workflow and graduation**

- Use `SOP.md` for how to capture notes across devices; keep drafts and footage lists out of this repo or in redacted form per `SECURITY.md`.
- **Graduation**: production moves to screenplay software, storyboards, and shoots—*not* this markdown repo. If they later build a website or tool for the film, *that* code gets a separate implementation repository with the usual safety rules.

## Example: Applying the Template to a Side Project
Use a concrete side project (such as the ForkIt experience) to demonstrate:
- Creating an initial spec.
- Setting up context and workflow.
- Deciding when (and how) to spin up an implementation repo.

For more background on how this template grew out of a real ForkIt codebase and its specs, see `advanced/ORIGIN_STORY.md`.

## See Also
If you want more code-generating or compiler-style spec workflows, explore:
- GitHub Spec Kit and related tools.
- Other spec-driven development projects that focus on turning markdown directly into code.
