---
description: Scaffold a new Polylith brick (component or base)
---

1. Ask the user for the name of the new brick.
2. Ask the user for the type of the brick (component or base).
3. Run `uv run poly create <type> <name>`.

// turbo
4. Add the new brick to the development project by editing `development/pyproject.toml` (if necessary, or just rely on `poly sync` if configured). Actually, `uv` workspace auto-discovery usually works, but it is good practice to ensuring it is buildable. 

Note: `uv run poly create` handles the directory creation. work in the root directory.
