# STRATA governance handoff

Snapshot: 2026-11-15 (America/Toronto), before SUN governance thread archival and memory cleanup. Reviewed main: `eb9b7e590e7d2506804254c70ade71c8ef035824`.

STRATA is SUN-G002, the stack-agnostic template. FOUNDRY (SUN-G003) provisions repositories/settings; SUN Ecosystem (SUN-G001) owns shared policy. STRATA is currently marked as a GitHub template repository. See [template guide](TEMPLATE-GUIDE.md), [setup checklist](REPOSITORY-SETUP.md), [optional asset preparation](ASSET-PREPARATION.md), and [brand guide](../branding/BRAND-GUIDE.md).

## Confirmed implementation and limits

- Template CI supplies `repository-validation` and PR `conventional-title`; it does not build an application stack. Generated products must add their own real CI and owners.
- Repository settings, rulesets, secrets, environments, approvals and workflow history are not transferred by template creation. Configure and verify them for every target.
- Asset preparation is opt-in/manual, artifact-only, and separate from branding ZIP installation. The disposable runner E2E test validates generator integration, not a live GitHub repository factory or production dispatch.
- Current branding uses approved PNG banner/symbol/icons; legacy vector references and archives remain. Merged [#6](https://github.com/sunstriker2009/sun-strata/pull/6) normalized the banner/reference layout; [#7](https://github.com/sunstriker2009/sun-strata/pull/7), [#8](https://github.com/sunstriker2009/sun-strata/pull/8) and [#9](https://github.com/sunstriker2009/sun-strata/pull/9) established the canonical symbol and raster exports.
- Fleet governance alignment was reported successful by the operator. This documentation review is not a new live ruleset audit.
- STRATA has no `branding-auto-install.yml` hook in the reviewed tree and no numbered revision snapshots. The merged live hook pilot belongs to ASTELVO [#39](https://github.com/sunstriker2009/sun-astelvo/pull/39), not STRATA.

## Pending, when explicitly resumed

Review whether STRATA should offer an optional branding ZIP hook after live rollback validation. Any adoption needs a reviewed pinned FOUNDRY action, appropriate repository/actor guards and workflow-dispatch CI behavior; copying ASTELVO's repository-specific guard unchanged would disable it in a generated repository. Keep template defaults explicit and product-neutral. Do not enable hooks or execute a branding installation merely to complete this handoff.

Legacy archive-to-revisions migration remains separate reviewed work. Revisions preserve complete asset snapshots; original concepts and provenance may need separate retention. New products must replace STRATA identity with their own approved artwork. PNG compact assets are allowed; vectors are optional reviewed adaptations where useful.

## Resume rules

Read current repository documentation and live GitHub state before acting; this snapshot is not a standing authorization to resume implementation or administrative changes. Preserve explicit pauses. Use feature branches and PRs, required checks, applicable human review and squash merges; never push directly to protected main or weaken protection to make a verifier pass. Batch related fixes, avoid duplicate CI and unnecessary reruns, and stay within the owner's free GitHub Actions budget. Never store tokens in documentation.

Before continuing, inspect open PRs, branch tips and latest workflow results. Distinguish implementation, operator-reported live validation and independently verified evidence. Re-run read-only checks when needed; do not infer current compliance from an old green report. Do not create disposable repositories, change settings, roll out hooks, migrate archives or resume paused product work just because it appears in a next-step list.
