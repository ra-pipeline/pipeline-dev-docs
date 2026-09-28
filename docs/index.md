# Pipeline Developer Documentation

An open, community-driven documentation and technical reference platform for radio astronomy data processing pipelines.

> **Community Platform & Independent Effort Notice**  
> This site is an independent, community-maintained knowledge base created by and for pipeline developers, researchers, and scientific software engineers. All contributions, architectural memos, and technical articles represent voluntary efforts conducted on personal time in an individual capacity, and do not represent official corporate or institutional documentation, nor work-for-hire on behalf of any employer.

The pipeline automates calibration and imaging for radio interferometric observations, combining CASA tasks with heuristic engines that dynamically derive processing parameters from observation metadata.

## Scope

- **Development**: Environment setup, workflow conventions, and local documentation builds.
- **Development Memos (PDM)**: Formal technical memos documenting architecture decisions, security policies, and technical investigations.

<!-- Under review - hidden from active index:
- **Architecture**: Core pipeline abstractions—contexts, tasks, domain objects, and heuristic engines.
- **Quality Assurance**: Testing tiers, regression benchmarks, and the operational distinction between software verification and scientific validation.
- **Knowledge Base**: Curated index of refereed publications, ADASS proceedings, and technical memos.
-->

## Navigation

- [Getting Started](getting-started.md): Environment setup, Git workflow, and previewing docs locally.
- [Development Memos](pdm/index.md): Pipeline Development Memo series, including [PDM 1: Agent Workflow Security](pdm/pdm-001-agent-workflow-security.md).

<!-- Under review - hidden from active index:
- [Architecture Overview](architecture/overview.md): High-level structure, pipeline stages, and the CASA interface layer.
- [Tasks & Heuristics](architecture/tasks-and-heuristics.md): Separation of procedural tasks and heuristic decision engines.
- [Quality Assurance Strategy](qa/strategy.md): Unit tests, regression suites, and acceptance benchmarks.
- [Verification vs. Validation](qa/validation-vs-verification.md): Guidelines on software verification vs. astronomical validation for releases and patches.
- [Knowledge Base](kb/index.md): Core publications, proceedings, and citations.
-->

## Local Preview

To preview documentation changes locally:

```bash
uvx zensical serve
```

This serves the site at `http://localhost:8000` with live reload. See [Getting Started](getting-started.md) for full setup options and contributing guidelines.
