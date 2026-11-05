# Concise Docs

An instruction-only skill for writing, reviewing and maintaining documentation across projects. Use it for READMEs, agent instructions, guides, plans, specifications and handoffs.

[SKILL.md](SKILL.md) contains the writing workflow and review rules. It keeps information authoritative, reading paths direct and instructions clear without losing constraints or evidence. It needs no scripts, services or project-specific dependencies. Code and configuration retain their own correctness requirements.

## Install in Codex

Clone this repository into a stable location, then link that checkout into the user skill directory:

```sh
git clone git@github.com:LasaleFamine/concise-docs.git "$HOME/src/concise-docs"
mkdir -p "$HOME/.agents/skills"
ln -s "$HOME/src/concise-docs" "$HOME/.agents/skills/concise-docs"
```

Choose an unused checkout path. If a `concise-docs` installation already exists, reconcile it with this checkout before linking; do not overwrite local changes or install duplicate copies. Pull repository updates into the same checkout to update the linked skill.

For team use, place the skill in the repository's `.agents/skills/concise-docs` directory. Other agents can use the same `SKILL.md` through their supported skill mechanism or by reading it explicitly. Discovery paths differ by runtime. [Codex skill documentation](https://learn.chatgpt.com/docs/build-skills).

## Use

Example requests:

- `Use $concise-docs to write an onboarding guide from this project's current setup commands.`
- `Use $concise-docs to assess our documentation reading paths and propose improvements.`
- `Use $concise-docs to simplify this runbook while preserving its operational constraints.`

To make it a project writing convention, add this to the project's agent instructions once the skill is available:

> When creating or updating documentation, apply concise-docs. Follow this repository's formats and requirements.

Automatic selection depends on the host and task description. Explicit invocation selects the skill for the requested work; an assessment alone does not request edits.

## Maintain

Keep reusable instructions in `SKILL.md` and Codex display metadata in `agents/openai.yaml`. Check changes against a new-document task, an assessment and an authorized revision. Verify links and preserve project-specific requirements. Keep personal paths, credentials and private project evidence out of the repository.
