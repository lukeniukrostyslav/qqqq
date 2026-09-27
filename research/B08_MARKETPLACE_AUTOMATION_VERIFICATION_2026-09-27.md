# B08 Current Marketplace + Automation Verification

Date: 2026-09-27

## GitHub Actions

GitHub documentation confirms that scheduled workflows:
- run from the latest commit on the default branch;
- use POSIX cron syntax;
- have a minimum interval of 5 minutes;
- can be delayed during high Actions load.

Source: https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows

B08 workflow hardening:
- removed dependence on github.event.head_commit.message for the job condition, because scheduled events do not provide a normal push commit payload;
- removed the keep-aspect-ratio option from the A4 raster command so the pipeline can deterministically produce the required 2480x3508 canvas and let repository QA reject anything else;
- binary delivery remains unapproved until the generated JPGs are actually present in GitHub.

## Etsy current digital-delivery constraints

Official Etsy Help currently states:
- up to 5 digital files per instant-download listing;
- maximum 20 MB per uploaded file;
- ZIP is supported;
- buyer-visible filenames are retained;
- digital filenames are limited to 70 characters using alphanumeric characters, periods, underscores, or hyphens.

Sources:
- https://help.etsy.com/hc/en-gb/articles/115015628347-How-to-Manage-Your-Digital-Listings
- https://help.etsy.com/hc/ru/articles/115015663347-%D0%A2%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BA-%D0%B8%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC-%D0%B2-%D0%BC%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0-Etsy

Etsy also currently recommends listing images at least 2000 px wide/high and does not support transparent PNGs as listing images; transparent areas display black. This affects previews, not the buyer's downloadable transparent PNG assets.

## B08 gate

Current approved commercial assets: 0/90.

The 20 journal-page masters are complete, and local raster QA previously passed 40/40 files. However, B08 progress is not raised until the generated 40 JPG binaries are confirmed in the GitHub repository and the delivery gate is rechecked.

Next gate: verify GitHub delivery presence -> verify workflow QA evidence -> approve 20 journal-page concepts -> update B08 to 20/90 = 22.22% only after the gate passes.

## 2026-09-27 workflow dispatch verification

Additional official GitHub documentation check:
- A workflow can be run manually only when the workflow file includes the `workflow_dispatch` trigger.
- The workflow file must exist on the repository's default branch for the manual trigger to be available.
- GitHub documents both the Actions UI and REST API as supported ways to dispatch a workflow.
- A workflow dispatch requires appropriate write access.

Sources:
- https://docs.github.com/en/actions/how-tos/manage-workflow-runs/manually-run-a-workflow
- https://docs.github.com/en/rest/actions/workflows

Repository change:
- Added `workflow_dispatch:` to `.github/workflows/b08-journal-raster-delivery.yml`.
- Added an Actions artifact upload step so a successful run leaves an independently inspectable verification artifact.
- Commit: `3d3f3d56f1c5c0b863ffb1a94b7884039def7a07`.

Current gate remains CLOSED:
- Expected GitHub JPG delivery files still return HTTP 404 through the GitHub contents API.
- Therefore approved commercial assets remain 0/90 and B08 remains 0%.
- No progress percentage is raised until the 40 JPG binaries are actually present and their technical QA is verified from the repository.

## 2026-09-27 live GitHub documentation re-check

Current official GitHub documentation confirms:
- `workflow_dispatch` exposes the manual **Run workflow** control when the workflow file is on the default branch.
- A manual workflow can be started from the Actions UI, GitHub CLI, or the REST workflow-dispatch endpoint.
- GitHub's current documentation also confirms that events generated using `GITHUB_TOKEN` do not create new workflow runs, except `workflow_dispatch` and `repository_dispatch`.
- Workflow execution policies can also restrict which actors/events are allowed to run Actions.

Sources checked:
- https://docs.github.com/en/actions/how-tos/manage-workflow-runs/manually-run-a-workflow
- https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows
- https://docs.github.com/en/rest/actions/workflows
- https://docs.github.com/en/actions/concepts/about-actions-policies
- https://docs.github.com/en/enterprise-cloud@latest/actions/concepts/security/github_token

Current repository evidence:
- The B08 workflow now contains `workflow_dispatch`.
- A controlled push was made to `proof/B08_JP_MASTERS/SL_JP_020_AGED_WRITING_PAGE.svg` to exercise the configured `push` trigger.
- No Actions-generated commit has appeared after that trigger yet.
- Expected JPG delivery files still return 404 through the GitHub contents API.

Conclusion:
The workflow definition is now prepared for deterministic manual execution, but the available GitHub connector in this session does not expose the REST workflow-dispatch action itself. Therefore no claim of a successful Actions run is made until GitHub provides run/artifact/file evidence.

B08 gate remains CLOSED: 0/90 approved commercial assets.
