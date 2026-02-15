# AGENTS.md

## Skills

### Available skills
- album-workflow: End-to-end workflow for creating and deploying a family album from a WhatsApp export folder. (file: `CLAUDE.md`)

### How to use skills
- Trigger: Use `album-workflow` when the user asks to create/deploy an album or provides a WhatsApp export folder.
- Execution: Follow the 3 phases in `CLAUDE.md` (curation, HTML build, deployment).
- Context: Use family name mappings from `CLAUDE.md` for quote attribution and event labels.
- Output conventions: Keep media paths relative, create a dedicated `album_<name>/` folder, and add `.gitignore` exceptions for referenced media.
