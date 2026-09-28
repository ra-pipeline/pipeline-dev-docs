# Pipeline Development Memos

Pipeline Development Memos (PDMs) document design decisions, technical standards, and operational guidelines for pipeline development. Memos capture technical discussions, trade-offs, and consensus across the team.

## Published Memos

| Memo | Title | Date | Last Updated | Status |
| :--- | :--- | :--- | :--- | :--- |
| [PDM 1](pdm-001-agent-workflow-security.md) | Sandboxing and Execution Safety for AI Coding Agents | 2026-09-28 | 2026-09-28 | Draft |
| [PDM 2](pdm-002-collaboration-platform-governance.md) | Connecting AI Agents to Jira, Confluence, and Bitbucket Safely | 2026-09-28 | 2026-09-28 | Draft |

<!-- Under review:
| [PDM 3](pdm-003-rag-design-knowledge-systems.md) | Offline Knowledge Retrieval and Ragdoll Adoption for Pipeline Development | 2026-09-28 | 2026-09-28 | Draft |
-->

---

## Memo Lifecycle

Every memo tracks its current status in the header:

| Status | Meaning |
| :--- | :--- |
| **Draft** | Work in progress; gathering early feedback. |
| **Proposed** | Ready for team review and discussion. |
| **Accepted** | Agreed upon and adopted by the team. |
| **Implemented** | Recommended tooling or workflow is in active use. |
| **Superseded** | Replaced by a newer memo. |
| **Withdrawn** | Shelved or closed without adoption. |

---

## Starting a New Memo

To propose a memo:

1. Create a new file in `docs/pdm/` named `pdm-XXX-<topic>.md`.
2. Include the standard header (`Memo Number`, `Date`, `Status: Draft`, `Area`, `Target Audience`).
3. Add it to the table above.
4. Open a pull request so the team can review and discuss it.
