# Getting Started

Welcome to the community-driven developer documentation platform for the pipeline development project. This guide covers environment prerequisites, previewing and building this site locally, and submitting community contributions.

## Prerequisites

- **Git**
- **[uv](https://github.com/astral-sh/uv)** (recommended for previewing docs and managing tools)
- **Python 3.10+** (if not using `uv`)

## Building and Serving Documentation

We use [Zensical](https://zensical.org) to generate this documentation site. The simplest way to run Zensical is with `uv`, which executes the tool directly without needing to configure a virtual environment or modify your system Python.

### Running a local preview server

Clone the repository and run `uvx zensical serve`:

```bash
git clone https://github.com/ra-pipeline/pipeline-dev-docs.git
cd pipeline-dev-docs
uvx zensical serve
```

Then open `http://localhost:8000` in your browser. Any edits made to files in `docs/` or `zensical.toml` will refresh automatically.

### Building the static site

To generate the static HTML files locally:

```bash
uvx zensical build --clean
```

The compiled output is placed in `site/`.

### Alternative installation options

If you prefer to install Zensical directly or run within a local virtualenv:

- **As a standalone tool with `uv tool`:**
  ```bash
  uv tool install zensical
  zensical serve
  ```

- **In a project virtual environment:**
  ```bash
  uv venv
  uv pip install zensical
  uv run zensical serve
  ```

- **With standard `pip`:**
  ```bash
  pip install zensical
  zensical serve
  ```

## Contributing Workflow

1. Create a feature branch from `main`:
   ```bash
   git checkout -b docs/my-topic-update
   ```
2. Add or update Markdown files in the `docs/` directory.
3. If you add new pages or reorganize sections, update the `nav` list in `zensical.toml`.
4. Check that the build completes without errors:
   ```bash
   uvx zensical build --clean
   ```
5. Commit your changes, push your branch, and open a Pull Request on GitHub.
6. The CI workflow in `.github/workflows/docs.yml` automatically verifies that the site builds cleanly.
7. Once merged into `main`, GitHub Pages will update automatically.
