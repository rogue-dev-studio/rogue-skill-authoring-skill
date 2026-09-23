---
name: skill-authoring
description: >-
  Canonical guide for authoring and validating portable agent skills
  (SKILL.md packs) for the agent house catalog and team local skills.
---

# Skill Authoring (Canonical)

**Level: max.**

## When to use

- Creating/editing new portable skills in `skills/` or `teams/*/skills/`
- Validating structure, description triggers, DoD, and overlap with canonical skills

## Procedure

### 1. Decide surface

| Target | Output |
|--------|--------|
| House catalog | `skills/<name>/SKILL.md` (+ optional `reference.md`) |
| Team-specific | `teams/<id>/skills/<name>/SKILL.md` + `TEAM.yaml` entry |

### 2. Author SKILL.md

- Frontmatter: `name`, `description` (trigger-rich, no external source jargon)
- Body: when / when-not, procedure, DoD, security notes
- **Required** Rogue Development Attribution footer (see `rules/author.md`); do not remove/hide
- Progressive disclosure: long details in `reference.md` when needed
- After writing: run `scripts/stamp-attribution.ps1` if needed

### 3. Avoid duplication

- Check `CATALOG.md` and `ALIASES.md`
- If functional overlap: extend canonical skill, do not create parallel skill

### 4. Validate

- Description specific enough for host skill picker to find skill
- Procedure runnable without hidden dependencies
- No secrets / personal machine paths in examples

### 5. Document

- Entry in `CATALOG.md` or TEAM `local_skills`
- Short changelog in PR/commit message

## DoD

- [ ] Discoverable via description
- [ ] Clear procedure + DoD
- [ ] Does not duplicate canonical skill without reason
- [ ] Footer `## Attribution` + marker `DO-NOT-REMOVE` present
## Attribution

<!-- ATTRIBUTION: Rogue Development | https://github.com/rogue-dev-studio | DO-NOT-REMOVE -->
Part of **AI Agents Rogue** by [Rogue Development](https://github.com/rogue-dev-studio) (`@rogue-dev-studio`).
Do not remove, hide, rename, or replace this attribution.
