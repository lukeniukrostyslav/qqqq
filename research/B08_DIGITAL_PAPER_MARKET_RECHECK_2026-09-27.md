# B08 Digital Paper Market Re-check — 2026-09-27

## Current market evidence

Current Etsy search results continue to show demand for dark-academia / vintage junk-journal paper products. Examples observed during this check include:
- A vintage library junk-journal paper listing offering 20 printable 300 DPI JPG papers plus bonus ephemera.
- A gothic arches background pack offering 6 printable JPG background pages.
- A dark-academia vintage text paper pack offering 10 printable background pages.
- A dark-academia printable kit offering 4 US Letter collage sheets.
- A mystical vintage journal-page listing offering 5 JPG files at 300 DPI.

These are market observations, not sales guarantees. Listing reviews and shop sales are signals, not exact unit-sales data for an individual SKU.

## Production implications for SECRET LIBRARY

1. Digital papers should remain a coherent supporting category rather than duplicate the journal-page layouts.
2. The 15-paper set should deliberately mix:
   - quiet filler textures;
   - archival/grid structures;
   - darker library surfaces;
   - muted green/burgundy accents;
   - manuscript and botanical textures.
3. Papers must remain usable as backgrounds: decoration should stay lower contrast than the writing-page category.
4. The master format is 3600x3600 SVG source with raster delivery at 3600x3600 JPG, 300 DPI.
5. File names remain ASCII-only and below marketplace filename limits.

## Marketplace packaging constraint

Etsy's current official help states that an instant-download listing can contain up to five digital files, with a maximum of 20 MB per file, and ZIP is supported. Therefore the eventual commercial package must be split/packed deliberately rather than assuming one unrestricted upload.

Sources:
- https://www.etsy.com/listing/4303043768/vintage-library-junk-journal-papers
- https://www.etsy.com/listing/1541247277/gothic-arches-junk-journal-paper-dark
- https://www.etsy.com/listing/4431429849/dark-academia-junk-journal-papers
- https://www.etsy.com/listing/1502417123/dark-academia-printable-junk-journal-kit
- https://www.etsy.com/listing/1406032944/mystical-vintage-journal-pages-digital
- https://help.etsy.com/hc/en-gb/articles/115015628347-How-to-Manage-Your-Digital-Listings

## Gate

Research does not increase B08 progress by itself. The 15 digital-paper concepts become approved only after the repository contains the generated JPG binaries and the automated technical QA passes.


## Workflow verification result

The first digital-paper-capable run reached and passed the full technical QA gate: the log reports **40 journal JPGs + 15 digital paper JPGs**, and the artifact upload completed with 55 files. The final failure occurred only at the Git push step because another repository commit had advanced `main` while the workflow was running. The generated local commit therefore could not fast-forward the remote branch.

This was a repository-concurrency issue, not an asset-rendering or QA failure. The workflow was hardened in commit `e2b9b920db148ea8a68ee56856841204091a545b` to fetch `origin/main`, rebase the generated delivery commit onto the current main, and then push. The B08 gate remains closed until the rebased generated commit is actually present in GitHub.
