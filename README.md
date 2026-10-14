# Paperclip agent-team configuration

Reusable role prompts and review-policy examples by Ibrahim Sabri Örene, generalized from a locally operated company-style agent team.

This repository contains **configuration**, not the Paperclip platform and not application source from any project the team worked on. All project names, private work items, internal documents, repository paths, agent identifiers, tokens and delivery context are omitted.

## Team structure

- **Tech lead:** defines scope and acceptance criteria, splits independent work, coordinates review.
- **Developer:** works in an isolated Git worktree, reproduces issues, implements and verifies changes.
- **QA reviewer:** independently checks the developer's branch and returns actionable findings.
- **Documentation/CI:** keeps accepted behavior and verification commands visible.

Cross-model review is preferred where useful. A developer should not be the only reviewer of their own work. Review rounds are bounded so the team can make an explicit decision instead of looping indefinitely.

## Use

Install and configure the existing [Paperclip platform](https://github.com/paperclipai/paperclip) according to its documentation. Create your own agents and point their instruction-file settings to the role files in `agents/`. Supply the target repository and its actual test commands through your own project context.

`examples/review-policy.json` illustrates the review/approval fields used by the local setup. Replace placeholder agent IDs with IDs from your own instance and verify support in your installed Paperclip version. This repository is not an automatic company-import bundle.

Use isolated execution workspaces for independent implementation tasks; serialize changes that touch the same files. Keep human authorization requirements and sensitive actions explicit. The example policy assigns routine review to the QA role and approval to the tech lead; configure separate human gates for actions that require them.

## Attribution and scope

Paperclip is an existing upstream project by its own contributors. This repository showcases my reusable team configuration only and claims no authorship of that platform. No new license grant has been selected for these prompts.
