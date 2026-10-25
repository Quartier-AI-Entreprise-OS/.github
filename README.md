# .github

Organization-wide defaults for Quartier AI Entreprise OS repositories.

GitHub applies the files in this repo to every repository of the organization that does not define its own file of the same type. The rule is per file type and all-or-nothing: a repo with its own `.github/ISSUE_TEMPLATE/` folder ignores every issue template here.

## Contents

| Path | Purpose |
| --- | --- |
| `.github/ISSUE_TEMPLATE/bug_report.yml` | Bug report form |
| `.github/ISSUE_TEMPLATE/feature_request.yml` | Feature request form |
| `.github/ISSUE_TEMPLATE/task.yml` | Task form (non-code work: research, spike, brainstorm, investigation) |
| `.github/ISSUE_TEMPLATE/config.yml` | Template chooser: blank issues disabled, link to Discussions |
| `.github/PULL_REQUEST_TEMPLATE.md` | Single PR template with sections to delete when not relevant |

## Conventions

- Issue titles have no prefix. The type is carried by a label, so branches created from issues stay clean (`73-hide-sector-from-dispatch-profile`).
- A Bug is something broken. A Feature is something to build. A Task is work that produces knowledge or a decision rather than code (research, spike, brainstorm, spec).
- A Feature must fit in one PR and must have verifiable acceptance criteria. A Task has an expected deliverable and usually closes with a comment, a doc or follow-up Features.
- A PR links its issue with `Closes #<n>` and ticks the same impact checklist as the Feature.

## Required labels

Issue forms apply labels automatically, but only if the label already exists in the target repository. Create these in every repo:

| Label | Color | Description |
| --- | --- | --- |
| `type: bug` | `#d73a4a` | Something is broken |
| `type: feature` | `#a2eeef` | New capability or improvement |
| `type: task` | `#0e8a16` | Research, spike, brainstorm or investigation |

Severity, priority, area and size are captured as form fields rather than labels so the label set stays small. Add labels for them later if filtering by them becomes necessary.

## Issue types

If organization issue types (Bug, Feature, Task) are enabled in the org settings, add `type: Bug` / `type: Feature` / `type: Task` at the top level of each form and the type will be set automatically.
