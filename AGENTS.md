# Agent Instructions

Quick reference for working on this repository.

## Python & Tooling: Always use `uv`

We use `uv` for all Python tasks. Avoid using `pip`, `venv`, or bare system `python`.

- **Live preview docs**: `uvx --python 3.12 zensical serve`
- **Build / validate docs**: `uvx --python 3.12 zensical build --clean`
- **Run one-off scripts**: `uv run python <script.py>` (or `uv run --with <dep> python ...` if packages are needed)

Always verify `uvx --python 3.12 zensical build --clean` runs without warnings before completing doc changes.

## Documentation Config (`zensical.toml`)

- The site uses [Zensical](https://zensical.org) with the Material theme.
- Navigation and theme settings live in `zensical.toml`.
- Theme features must be defined as a flat list under `[project.theme]`, not nested subtables:
  ```toml
  [project.theme]
  features = [
      "navigation.tabs",
      "navigation.sections",
      "navigation.expand",
      "navigation.indexes",
      ...
  ]
  ```
- New PDM documents belong in `docs/pdm/` and automatically collapse under the Development Memos section when `navigation.indexes` is enabled.

## Common Sense Safety

- Don't run `rm -rf` or destructive deletions without asking first.
- Never force-push (`git push --force`) or rewrite shared branch history.
- Never dump or print secrets, tokens, or private credentials to the terminal or logs.
