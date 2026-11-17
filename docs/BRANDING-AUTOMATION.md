# Branding upload automation

Inherited by repositories generated from STRATA through FOUNDRY. On a feature branch containing `.github/workflows/branding-auto-install.yml`, the SUN owner commits one originally named ZIP directly under `branding/revisions/`. The pinned shared FOUNDRY action validates and installs assets in a follow-up commit on that branch, preserving numbered revision snapshots. Review artwork and required checks before squash merge. No main writes, PAT, schedule or automatic artwork merge is introduced.

The owner guard is intentionally restricted to sunstriker2009; other template users must explicitly review and adapt it. CI and PR-title workflows support workflow_dispatch because GITHUB_TOKEN-authored commits suppress ordinary workflow events. If a PR is open, the action dispatches both baseline checks on the installed commit. New stack-specific required checks must also be made dispatch-capable and added to validation-workflows in the hook. Do not remove or bypass required checks.

Template updates affect newly generated repositories only. Existing branches need the hook before the ZIP push; an old upload event is not replayed. If necessary, merge main into the upload branch and make a new owner push touching the pending ZIP. Numbered vN.zip snapshots are not uploads.

Full package requirements, revision behavior and recovery: https://github.com/sunstriker2009/sun-foundry/blob/main/docs/BRANDING-ZIP-INSTALLER.md
