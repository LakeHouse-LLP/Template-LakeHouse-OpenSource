# Changelog

## 0.1.0

### Minor Changes

- [#5](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/5) [`3802076`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/38020768dd75b5916ff975024e080965f78fd396) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Contributor growth: CONTRIBUTING/Codespaces, GOVERNANCE/ROADMAP, starter issues, listings, maintainer playbook, all-contributors, and SHA-pinned welcome workflow.

- [#3](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/3) [`d000ac3`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/d000ac39d646edae55b6c5aa7dc8f18879fccfd9) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Add the flagship public release system: changesets, CI-only `vX.Y.Z` tags, draft GitHub Releases with checksums and build provenance, and npm OIDC trusted publishing.

- [#4](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/4) [`185bb65`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/185bb65c20498781fe95810fc8e8c54cdb842c05) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - SEO and discoverability: dark-only brand kit (accent #7DFFFF), social preview, keyword-rich README, discoverability CI, and docs for Astro Starlight / launch channels.

### Patch Changes

- [#11](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/11) [`7ea1509`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/7ea150909cebc7f5c0fe9c25f95a06fe3d5a881d) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Brand kit v0.3: README picture header, palette (#1E1E1E / #7DFFFF / Geist), writing-style copy lint.

- [#15](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/15) [`ce152a1`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/ce152a12b48632becb26d7be6896a3235b2eca38) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Continuous self-improvement house rule: AGENTS note, docs/lessons.md log, PR template section; fix welcome first-interaction snake_case inputs.

- [#16](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/16) [`a8fe4ef`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/a8fe4ef97c1552a79b8a36075ba7fdbbfdc4abc0) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - CI: skip Dependabot for strict changelog and changeset status; welcome skips bots; Dependabot gets skip-changelog; refresh AUTO metadata after repo rename.

- [#10](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/10) [`00347bc`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/00347bcabbfe808465c1e8947df5cd5c05a337ab) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Prefer GitHub merge queue on public main; add merge_group triggers to required workflows and document stack/queue flow for Sen-only enqueue.

- [#9](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/pull/9) [`3a10120`](https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/commit/3a10120337a319f87bf8efb4177d0299c2cf491c) Thanks [@zsenarchitect](https://github.com/zsenarchitect)! - Document Vercel Shared Environment Variables rule (pointer to org canonical) and ban agent-managed `vercel env` changes without Sen approval.

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Initial **Template-OpenSource** scaffold (CI, OpenSSF Scorecard, CodeQL, DCO, gitleaks, README autogen, tier and runner guards). General-purpose OSS starter — no LakeHouse widget concepts.
- `.lakehouse/org.json` identity (orgName / brand / packageScope / domain) and `.lakehouse/pins.json` action + reusable-workflow catalog.
- Org-slug lint (`check:org-slug`), action-pin check (`check:pins`), and CITATION.cff generation from org.json.
- `docs/org.md` pointing at the organization `.github` runbook.
- Flagship release system: changesets, CI-only `vX.Y.Z` tags, draft GitHub Releases with SHA256 checksums and `attest-build-provenance`, npm OIDC trusted publishing, release-notes template, `.github/release.yml`, `docs/media/` convention, pre-release checklist, and rollback/yank docs.
- SEO / discoverability: dark-only `brand/` (accent `#7DFFFF`), social preview, keyword-rich README, `CITATION.cff`, docs for org Astro Starlight site, launch/awesome/search checklists, and `check:discoverability` CI (GitHub-hosted).
- Contributor growth: friendly CONTRIBUTING + Codespaces, ROADMAP/GOVERNANCE/SUPPORT, good first issue seeding guide, listings guide, maintainer playbook, all-contributors, and SHA-pinned welcome workflow (no PR checkout).
- Vercel env-var rule pointer (`docs/deploy/vercel-env.md`) + AGENTS Never-do; canonical detail in org `.github`.
- Merge queue preference for public `main`: `merge_group` on required workflows; CONTRIBUTING / AGENTS / Sen-only ruleset checklist (merge commits only).
- Brand kit v0.3 subset: `brand/readme-header` README `<picture>`, palette base `#1E1E1E` / accent `#7DFFFF` / Geist, docs-site theme notes, WRITING-STYLE rules in AGENTS/CONTRIBUTING, and `check:writing-style` CI.
- Continuous self-improvement: AGENTS house rule, [`docs/lessons.md`](./docs/lessons.md) log, and **What did we learn?** on the PR template.
- Welcome workflow: `first-interaction` v3 snake_case inputs (`issue_message` / `pr_message` / `repo_token`).

### Fixed

- Remote URL parsing avoids host substring checks (CodeQL).
- Lychee config uses `include_mail = false` (CLI no longer accepts `--exclude-mail`).
- Dependency-review Action deferred until the owner enables Dependency graph (agents do not change settings).
- Guards, README AUTO badges, and citations no longer hardcode the GitHub org slug (brand + custom domain instead).
- `org.json` domain is `REPLACE_WITH_CUSTOM_DOMAIN` (no assumed hostname); brand set to `LakeHouse`.
- Changeset status on PRs compares against the PR base ref so stacked PRs validate.
- Dependabot PRs: skip strict changelog and changeset-status checks; welcome skips bots; Dependabot applies `skip-changelog`.
- README AUTO / CITATION / changelog compare URL track the GitHub repository name from the remote (after rename).

[Unreleased]: https://github.com/LakeHouse-LLP/Template-LakeHouse-OpenSource/compare/HEAD...HEAD
