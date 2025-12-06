# Python Polylith Template (uv + hatchling)

A generic "Golden Path" repository template for a Python Polylith project managed by `uv`.

## Features

- **Dependency Management**: [uv](https://github.com/astral-sh/uv)
- **Build Backend**: [hatchling](https://github.com/pypa/hatch)
- **Architecture**: [Polylith](https://polylith.gitbook.io/polylith)
- **Agent-Ready**: Includes pre-configured rules and workflows for AI agents.

## Getting Started

1.  **Clone the repository** (or use as a template).
2.  **Install uv**: Ensure you have `uv` installed.
3.  **Sync dependencies**:
    ```bash
    uv sync
    ```

## Development

- **Run tests**:
    ```bash
    uv run poly test
    ```
- **Lint**:
    ```bash
    uv run ruff check .
    ```
- **Add a new component**:
    ```bash
    uv run poly create component <name>
    ```
- **Add a new base**:
    ```bash
    uv run poly create base <name>
    ```

## Structure

- `bases/`: Entry points (APIs, CLIs, etc.).
- `components/`: Encapsulated logic (bricks).
- `projects/`: Deployment configurations.
- `development/`: Sandbox for development tools.
- `.agent/`: Rules and workflows for AI coding assistants.
