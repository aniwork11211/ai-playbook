# Model routing

Pick the kind of model, then give it this vault. The tool name can change. The job does not.

Vault: `C:\Users\ANISH\Documents\ai-playbook`

## Jobs

| Job | Use when | Hand it |
| --- | --- | --- |
| Coding agent in the repo | Edits, runs, and tests files in a project | The repo, plus `INDEX.md` |
| Long-context writer | Long docs, synthesis, or reading many files without editing the repo | `INDEX.md` and the one writing or research file |
| Design or image model | Screens, brand images, or a visual direction before code | The frontend section of `skill-catalog.md` |
| Fast cheap model | A draft, a sort, a rewrite, or a first summary | The one file that holds the format you want |
| Second-opinion model | A check on a plan, a diff, or a risky choice | The same brief plus the one relevant file. Do not give it the whole vault |

## Installed second-opinion skills

- Codex: `C:\Users\ANISH\.claude\skills\consult-codex\SKILL.md`
- z.ai: `C:\Users\ANISH\.claude\skills\consult-zai\SKILL.md`

Use those when the coding agent can launch them. Otherwise paste the brief into the other model yourself.

## A model with no skill loader

1. Paste `C:\Users\ANISH\Documents\ai-playbook\adapters\ANY-MODEL.md`, or tell the model to read that file.
2. It reads `INDEX.md`, then only the one file the task needs.
3. If it cannot read this disk, paste `INDEX.md` and that one file into the chat.

ChatGPT, Codex, a local model, and any later tool use this same path. Add a new adapter file only when a tool has its own memory file worth a short pointer.
