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

## Git & Review Policy

- **Do NOT automatically commit or push**: Never run `git commit` or `git push` autonomously. Always keep changes in the working directory and wait for explicit human review and confirmation before committing or pushing.
- **Verify first**: Always test and verify changes (e.g., `uvx --python 3.12 zensical build --clean`) and summarize modified files for the reviewer.
- **No destructive operations**: Never run `rm -rf` or delete files without explicit confirmation.
- **No history rewrites**: Never force-push (`git push --force`) or rewrite branch history.
- **Secret hygiene**: Never print or leak secrets, tokens, dotfiles, or credentials to output streams.
