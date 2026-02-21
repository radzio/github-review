# github-review

Claude Code plugin that triages GitHub PR review comments — analyze, plan, and reply.

## What it does

1. Fetches inline review comments, top-level review bodies, and general comments via `gh`
2. Reads referenced files for context
3. Categorizes each comment: **Actionable**, **Informational**, **Already addressed**, or **Needs clarification**
4. Produces a consolidated action plan
5. Optionally posts clarification replies directly to review threads

## Install

### Via marketplace (recommended)

```bash
claude plugin marketplace add https://github.com/radzio/plugin-patisserie
claude plugin install github-review
```

### Standalone

```bash
claude plugin add https://github.com/radzio/github-review
```

## Usage

On a branch with an open PR, run:

```
/triage
```

## Prerequisites

- [gh](https://cli.github.com/) — `brew install gh`
- [jq](https://jqlang.github.io/jq/) — `brew install jq`
- Authenticated with GitHub: `gh auth login`
