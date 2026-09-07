[README.md](https://github.com/user-attachments/files/31920906/README.md)
<div align="center">

# a2a-workflow

**A lightweight Python scaffold for building Agent-to-Agent (A2A) communication workflows.**

Built on [`a2a`](https://pypi.org/project/a2a/) and [`a2a-sdk`](https://pypi.org/project/a2a-sdk/), served with [Starlette](https://www.starlette.io/) and [Uvicorn](https://www.uvicorn.org/), with real-time streaming via [SSE](https://pypi.org/project/sse-starlette/).

[![Python](https://img.shields.io/badge/python-3.12%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Managed with uv](https://img.shields.io/badge/managed%20with-uv-orange)](https://docs.astral.sh/uv/)

</div>

---

## Overview

`a2a-workflow` provides a minimal, production-ready foundation for developers building agents that communicate using the A2A protocol. It ships with a clean project structure, locked dependencies, and an ASGI server setup — so you can focus on agent logic instead of boilerplate.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Features

- 🔌 **A2A-ready** — built on the official `a2a` and `a2a-sdk` libraries
- ⚡ **ASGI-powered** — served via Starlette + Uvicorn for high performance
- 📡 **Streaming support** — Server-Sent Events (SSE) out of the box
- 📦 **Fast, reproducible installs** — dependency management via `uv` and a committed lockfile
- 🧩 **Minimal footprint** — clean starting point with no unnecessary boilerplate

## Requirements

| Tool   | Version |
|--------|---------|
| Python | 3.12+   |
| uv     | latest  |

Install `uv` if you don't already have it:

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Verify:

```bash
uv --version
```

## Installation

```bash
# 1. Clone the repository
git clone <(https://github.com/saqibmasoodai-ops/A2A-WORKFLOW)>
cd a2a-workflow

# 2. Install dependencies (creates a virtual environment automatically)
uv sync
```

> `uv sync` reads `uv.lock` and installs the exact dependency versions used in development — no surprises across machines.

## Usage

Run the application with `uv` (no manual environment activation required):

```bash
uv run main.py
```

Expected output:

```
Hello from a2a-workflow!
```

<details>
<summary>Prefer to activate the environment manually?</summary>

```bash
# macOS / Linux
source .venv/bin/activate

# Windows
.venv\Scripts\activate

# Then run
python main.py
```

</details>

## Project Structure

```
a2a-workflow/
├── main.py             # Application entry point
├── pyproject.toml      # Project metadata and dependencies
├── uv.lock             # Locked dependency versions
├── .python-version     # Pinned Python version (3.12)
├── LICENSE              # MIT License
├── .gitignore
└── README.md
```

## Dependencies

| Package         | Purpose                                        |
|-----------------|-------------------------------------------------|
| `a2a`           | Core Agent-to-Agent protocol library            |
| `a2a-sdk`       | SDK for building A2A-compliant agents           |
| `starlette`     | Lightweight ASGI web framework                  |
| `uvicorn`       | ASGI server for running the application         |
| `sse-starlette` | Server-Sent Events (SSE) support for streaming  |

## Development

```bash
# Sync dependencies after pulling changes
uv sync

# Add a new dependency
uv add <package-name>

# Remove a dependency
uv remove <package-name>

# Re-lock after editing pyproject.toml manually
uv lock

# Run any command inside the project's environment
uv run <command>
```

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to open a pull request or file an issue.

## License

This project is licensed under the [MIT License](LICENSE).
