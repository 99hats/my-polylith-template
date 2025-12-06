# Polylith Architecture Rules

1.  **Code Location**:
    *   All domain logic and shared code MUST reside in `components/` or `bases/`.
    *   `components/` are for encapsulated logic (bricks).
    *   `bases/` are for entry points (APIs, CLIs, Lambda handlers, Workers) that expose components to the outside world.

2.  **Project Configuration**:
    *   Projects in `projects/` are STRICTLY for deployment configuration (pyproject.toml).
    *   They MUST NOT contain source code (except for a minimal `__main__.py` if absolutely necessary, but prefer `bases`).
    *   They aggregate components and bases using `tool.uv.workspace]`.

3.  **Dependency Management**:
    *   ALWAYS use `uv add` to manage dependencies.
    *   Components should define their own dependencies in their `pyproject.toml` (if strictly isolated) AND/OR dependencies should be added to the project `pyproject.toml` that uses them.
    *   For this template, we follow the "loose" theme where workspace dependencies are often shared, but `uv` allows for per-project lockfiles.

4.  **Brick Creation**:
    *   Use `uv run poly create component <name>` or `uv run poly create base <name>` to create new bricks.
    *   After creating a brick, remember to add it to the `development` project to enable IDE support and testing.
