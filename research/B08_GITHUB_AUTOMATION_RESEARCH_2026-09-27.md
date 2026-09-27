# B08 GitHub Automation Research — 2026-09-27

## Current findings

- GitHub Actions supports scheduled workflows using POSIX cron. The minimum supported schedule interval is every 5 minutes, and scheduled workflows run from the latest commit on the default branch.
- A workflow can request `contents: write` permission when it needs to commit generated files back to the repository.
- GitHub documents that events caused by the repository `GITHUB_TOKEN` do not recursively start another workflow run; `workflow_dispatch` and `repository_dispatch` are exceptions.

## Application to B08

The journal raster workflow was first configured for `push`, but the connected GitHub write path did not produce a verifiable raster run. The workflow was therefore corrected and given a temporary 5-minute schedule so the repository can execute the generation independently of the connector's write event.

The workflow itself contains repository-level QA before committing any JPGs. B08 progress remains unchanged until the 40 JPGs are actually present in GitHub and re-verified.

Sources: GitHub Actions workflow syntax and trigger documentation (checked 2026-09-27).