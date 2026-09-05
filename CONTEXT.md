# wmariuss/awesome-devops context
> refreshed 2026-09-05 | upstream default: main @ d7f166f

## Identity & policies
- upstream: wmariuss/awesome-devops, default branch `main`, an awesome-list (Markdown; GitHub reports `Python` for its mkdocs/invoke tooling, but content is all markdown), English-first (README + all issues English).
- license: CC0-1.0.
- CLA/DCO: none. signed commits required: no (no branch protection on main; `web_commit_signoff_required: false`).
- AI-assisted PR policy: unstated — CONTRIBUTING.md has no AI/LLM/bot mention; org `wmariuss/.github` default health files absent (404). No `ai-generated`/`no-ai` labels.
- PR template: none (root/docs/.github searched; vetted passport `pr_template_present: false`).
- external tracker: GitHub. PR body: pipeline fallback 3-section shape.
- CODEOWNERS: `* @wmariuss` (sole maintainer Marius Stanca).

## Conventions (verified from merged PRs)
- Branch naming: merged headRefNames are mixed (`main`, `patch-1`, `add-sbproxy`, `add-qovery`, `feat/add-kubestellar-console`); no single dominant pattern -> fall back to `type/desc` (e.g. `fix/dead-links`).
- Commit style: plain imperative sentences are the norm ("Add X...", "Update Oxmgr entry in README.md", "Remove Chrome extension link per review feedback"); occasional conventionals ("docs: fix typo in URL", "feat: add ..."). Match imperative-style human commits.
- CONTRIBUTING format for entries: `[RESOURCE](LINK) - DESCRIPTION.`, description <80 chars ending in a full stop; one commit per category; imperative PR titles (e.g. "Update ...", "Add ...").
- CI: `.github/workflows/deploy.yml` builds mkdocs + gh-deploys on main push; `links-validator.yml` runs lychee on a hand-set cron + workflow_dispatch/repository_dispatch (cron string is invalid -> has not auto-run recently; last link-report issues are from 2025-09). Neither workflow triggers on PR, so fork PRs get no substantive CI checks.
- How outside PRs get merged: responsive-ish, batched. Merged external PRs (2026): #359 (Jul), #394/#412 (Jun), #413 (Jun), #403/#397 (Apr/May), and a batch closed 2026-03-30 (#368 URL typo fix, #372, #365, #364). Many are "Add <tool>" resource additions and occasional URL/doc fixes (#368 "docs: fix typo in URL").

## Maintainer picture
- Sole maintainer/owner: wmariuss (Marius Stanca). Single CODEOWNER. Review latency is uneven (batch closures), but external small PRs (including a single URL-typo fix, #368) do get merged.

## Issue-area health
- 192 open issues; the open set is dominated by "Add <tool> to <section>" suggestions (essentially PR requests) plus dependabot dep bumps. No maintainer-engaged bug/dead-link issue is open: the "links validator" label has 162 entries but every one is a closed "Automated Links Checker Report" from 2025 (the monthly checker's cron is broken and has not produced new reports since ~Sep 2025).
- For a dead-link fix there is no issue to attach to; treat as a self-found gap (repo-audit, Docs dimension).

## Gap ledger (dedupe — READ FIRST, never re-pick)
- 2026-09-05 self-found dead links (Cirrus CI org->com, Merlinn repo 404) — outcome: pr-opened (#1 https://github.com/olitreadwell/awesome-devops/pull/1) — README.md links were dead; deduped: no upstream issue/PR touched these lines.

## Mined gaps (discovered, not yet attempted)
- 2026-09-05 docs: README.md "Continuous Integration & Delivery -> Public Services" `https://cirrus-ci.org/` fails DNS (SERVFAIL via dns.google); canonical live URL is `https://cirrus-ci.com/` (resolves, Wayback 200 on 2026-05-23; project's own repos reference it). — status: fixed (link swapped).
- 2026-09-05 docs: README.md "Observability and Monitoring" `https://github.com/merlinn-co/merlinn` returns 404 and org+domain (`merlinn.co`) are both gone (project defunct, no successor); replaced with verified-200 Wayback snapshot (2024-07-27). — status: fixed (link swapped).
