# Repository Guidelines

This repository packages one Codex skill: `skills/prism`.

## Project Structure

- `skills/prism/SKILL.md` is the required skill manifest and instruction file.
- `skills/prism/template.html` is the reusable output template.
- `skills/prism/references/` contains reference material loaded only when needed.
- `skills/prism/assets/` contains output resources such as fonts.
- `skills/prism/agents/openai.yaml` contains UI metadata.

## Maintenance

- Keep the skill directory hyphen-case and keep the manifest `name` as `prism`.
- Keep `SKILL.md` focused on agent instructions; put large examples or catalogs in `references/`.
- Do not commit runtime logs, sessions, `.DS_Store`, credentials, or generated one-off HTML outputs.
- If template behavior changes, make sure `SKILL.md` and `template.html` still agree.

## Validation

Run this from the repository root:

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py skills/prism
```

For resource changes, also inspect the file list before publishing:

```bash
find skills/prism -maxdepth 4 -type f | sort
```
