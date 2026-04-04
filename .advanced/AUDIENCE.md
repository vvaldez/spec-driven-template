# AUDIENCE.md — Who this repository is talking to

This file maps **two roles** relative to *this template repository*. It complements [`.advanced/PERSONAS.md`](PERSONAS.md): personas describe **how much** to read and your comfort level; this file describes **your relationship** to the repo (template consumer vs template steward).

## Two roles in this repository

| Role | You are… | Same idea, other words (use any; they mean the same here) |
| --- | --- | --- |
| **Template user** | Using this copy of the repo to plan **your** outcome—`SPEC.md`, context files, workflows. You read the template docs as a **consumer** of the template. | Fork user, clone user, downstream user, “planning in my copy,” “using the template for my own work” |
| **Template maintainer** | Changing the **shared** template so **other** copies inherit your edits (this upstream repository’s docs and structure). | Maintainer, template contributor, template editor, upstream maintainer |

When **AI assistants** say “you” without more detail, they default to **template user** unless you state you are maintaining the template—see root [`AGENTS.md`](../AGENTS.md).

**Checklists:** **Template users** use **root [`TODO.md`](../TODO.md)** for project next steps. **Template maintainers** use **[`.dev/TODO.md`](../.dev/TODO.md)** for upstream template milestones—do not mix them.

---

## Product audience (who your spec is for—not the template)

**Template user** is **not** the same as **who your planned outcome serves**.

- **Product audience** (also **spec audience**): the people, customers, players, readers, or stakeholders **for the thing you are describing** in [`SPEC.md`](../SPEC.md). Sections like **Personas / Users** in `SPEC.md` usually mean **them**, not people reading this template.

When docs or placeholders say “user,” check **which** user: **template documentation** (you as template user) vs **your product** (your product audience).

### Optional: add your product audience here (template users)

_Use this space if it helps collaborators and assistants. Examples: “Primary readers: …”, “Players who …”, “Internal ops team …”. Keep it short; long form can stay in `SPEC.md`._

---

## Related

- [`PERSONAS.md`](PERSONAS.md) — depth and reading paths (Personas 1–4)
- [`README.md`](../README.md) — onboarding
- [`DEV.md`](../DEV.md) — maintainer scope and workflow
- [`INTENT.md`](../INTENT.md) — charter, including explicit vocabulary
