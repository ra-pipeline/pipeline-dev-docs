# Pipeline Developer Documentation

An open, community-driven documentation and architecture reference platform for radio astronomy data processing pipelines. Built with [Zensical](https://zensical.org) and published to GitHub Pages via GitHub Actions.

> [!NOTE]
> This platform is an independent, community-maintained knowledge base created by and for pipeline developers, researchers, and scientific software engineers. It is a community-driven initiative and does not represent official corporate or institutional documentation.

## Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── docs.yml       # GitHub Actions build and Pages deployment
├── docs/                  # Markdown documentation source files
│   ├── index.md           # Homepage
│   ├── getting-started.md # Developer setup guide
│   ├── architecture/      # Pipeline task and heuristic architecture
│   ├── qa/                # QA strategy, verification vs validation
│   ├── pdm/               # Pipeline Development Memos
│   └── kb/                # Literature and technical memo references
├── zensical.toml          # Site configuration and navigation
└── README.md
```

## Local Development

We recommend using [uv](https://github.com/astral-sh/uv) to preview or build the site without needing to manage a virtual environment:

### Live preview
```bash
uvx zensical serve
```
Open `http://localhost:8000` in your browser. Changes to `.md` files or `zensical.toml` will reload automatically.

### Build static site
```bash
uvx zensical build --clean
```
The output is written to `site/`.

If you prefer a persistent install, you can also install Zensical with `uv tool install zensical` (or `pip install zensical`).

## Deployment

The GitHub Actions workflow in [`.github/workflows/docs.yml`](.github/workflows/docs.yml) handles CI and deployment:

- **Pull Requests**: Runs `zensical build --clean` to check for broken links and configuration issues.
- **Pushes to `main`**: Builds and deploys the static site to GitHub Pages.

To enable GitHub Pages in the repository:
1. Go to repository **Settings** -> **Pages**.
2. Under **Build and deployment** -> **Source**, select **GitHub Actions**.
3. Pushes to `main` will deploy automatically.

## AI Assistance Disclosure

Portions of this documentation and initial draft scaffolding were developed with the assistance of AI coding assistants.

All technical specifications, architectural designs, and operational policies have been reviewed, edited, and validated by human maintainers. Human contributors retain full responsibility for the accuracy, security, and integrity of the content published here. No proprietary credentials, private tokens, or confidential datasets were exposed in the preparation of these documents.

## Independent Community Effort & Personal Capacity Disclaimer

This project is an independent open-source documentation and knowledge-sharing platform:

- **Personal Effort**: All contributions, documentation, architectural memos, and configuration in this repository represent the independent, voluntary efforts of individual contributors acting strictly in their personal capacities.
- **Outside Official Working Hours**: Work on this project is conducted entirely during personal, off-duty time, using personal equipment, without the use of employer resources, facilities, or funding.
- **Not Work-for-Hire**: Contributions are not commissioned, assigned, supervised, or endorsed by any current, past, or future employers of the contributors.
- **No Institutional Affiliation**: Opinions, designs, and recommendations expressed herein are solely those of the individual authors and do not reflect the official positions, policies, or technical roadmaps of any employer, institution, or observatory.

## License

This repository is dual-licensed:

- **Documentation & Written Content**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
- **Code & Configuration**: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Pipeline Contributors. See [LICENSE](LICENSE) for details.
