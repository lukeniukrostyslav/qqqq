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