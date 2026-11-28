# AGENTS.md

Rules for AI-assisted contributions to the repositories under
[`nyuchiGOV`](https://github.com/nyuchiGOV). This org's `.github` repository
keeps its agent rules in `AGENTS.md` only: no `CLAUDE.md` and no `.claude/`
directory. Claude Code, Cursor, Copilot and other agents read this one file.

The org-wide guide is
[`nyuchi/.github` AGENTS.md](https://github.com/nyuchi/.github/blob/main/AGENTS.md).
Read it first; this file adds what is specific to government services, and
a repository's own `AGENTS.md` wins over both where they conflict.

## What this repository is

The community-health defaults for every `nyuchiGOV` repository that does not
carry its own: `SECURITY.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`,
`SUPPORT.md` and `.github/PULL_REQUEST_TEMPLATE.md`. It holds no application
code. Its other files (`.prettierrc`, `.markdownlint.jsonc`, `.yamllint.yaml`)
configure the org lint checks.

## Working here

- Every pull request targets `main`, the only long-lived branch, with a
  Conventional Commits title and a `Closes #n` or `Refs #n` line.
- Keep the files short and real. No placeholder text, and no wording copied
  from another org that names its products.
- Run `npx prettier --check .` and `npx markdownlint-cli2 "**/*.md"` before
  you push. The org lint workflow runs the same checks.
- A change to `SECURITY.md` changes the reporting promise made to people who
  find a vulnerability in a government service. Do not weaken it, and do not
  change the contact address without the owner's decision.

## Government services: extra care

- The services these repositories build handle personal data of travellers
  and citizens. Never put real personal data, passport or identity numbers,
  credentials or tokens in an issue, a pull request, a fixture or a log.
  Use clearly fake test values.
- Do not change deployment, DNS, hosting or access settings from a
  documentation pull request.
- Report anything that looks like exposed personal data privately through
  [`SECURITY.md`](./SECURITY.md), never in a public issue.
