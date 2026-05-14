# Deploy Party demo target

This repo is the **target** for the [Deploy Party](https://github.com/CoveHealth/deploy-queue-50000) POC.
It contains:

- `.github/workflows/ci.yml` — green-passing PR check so PR validation succeeds.
- `.github/workflows/deploy-staging.yml` — `workflow_dispatch`-triggered staging stub. The Deploy Party app fires this when a party transitions out of `forming`.
- `.github/workflows/deploy-prod.yml` — same shape for prod. Fired after every member signs off staging.
- `db/migrations/` — present so the migration-detection code path has a real prefix to look at.

Open PRs are mergeable by design. Merging happens automatically through Deploy Party — don't merge them manually.
