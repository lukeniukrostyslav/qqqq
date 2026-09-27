# B08 — Asset Creation Manifest

Дата: 2026-09-27

## Purpose

This manifest is the production checklist for SKU 001:
**SECRET LIBRARY — Dark Academia Journaling Kit**

B08 is not complete until every planned asset has either:
- been created;
- passed visual/technical checks;
- received its permanent ID;
- been recorded here.

No asset is counted merely because it is planned.

## Target inventory

| Category | Target |
|---|---:|
| Journal Pages | 20 |
| Digital Papers | 15 |
| Ephemera | 20 |
| Decorative PNG | 20 |
| Tags / Bookmarks | 10 |
| Bonus | 5 |
| **TOTAL** | **90** |

## Status legend

Current proof status: **75 APPROVED assets / 90 planned**

- PLANNED — specification exists, asset not created.
- DRAFT — first version created, not approved.
- REVISION — failed a check and is being corrected.
- APPROVED — passed the B08 production checks.
- REJECTED — removed from production.

## Journal Pages

| ID range | Count | Status |
|---|---:|---|
| SL_JP_001–020 | 20 | APPROVED |

Initial concepts:
001 Library Catalogue
002 Reading Log
003 Chapter Notes
004 Bookplate
005 Research Notes
006 Archive Record
007 Private Collection
008 Marginalia
009 Correspondence
010 Book Review
011 Quote & Citation
012 Reading List
013 Secret Index
014 Scholar Notes
015 Library Visit
016 Character Notes
017 Plot / Story Notes
018 Antique Ledger
019 Chapter Divider
020 Aged Writing Page

## Digital Papers

| ID range | Count | Status |
|---|---:|---|
| SL_DP_001–015 | 15 | APPROVED |

Initial concepts:
aged parchment, charcoal paper, faded ledger, subtle book-page texture, archival beige, muted green paper, muted burgundy accent paper, dark library texture and restrained seamless motifs.

## Ephemera

| ID range | Count | Status |
|---|---:|---|
| SL_EP_001–020 | 20 | APPROVED |

Initial concepts:
library card, catalogue slip, accession label, envelope, ticket, archive note, bookplate, due-date card, manuscript fragment, stamp, receipt, index card, small label set, bookmark insert, correspondence fragment, collection tag, research note, archive seal, shelf label, private-library card.

## Decorative PNG

| ID range | Count | Status |
|---|---:|---|
| SL_PNG_001–020 | 20 | APPROVED |

Initial motifs:
antique key, closed book, stacked books, ink bottle, quill, candle, candleholder, antique frame, magnifying glass, botanical specimen, pressed leaf, raven silhouette, old clock, brass lock, ribbon, wax-seal-style ornament, reading glasses, compass, small lantern, book stack with bookmark.

All must be original and non-branded.

## Tags / Bookmarks

| ID range | Count | Status |
|---|---:|---|
| SL_TB_001–010 | 10 | PLANNED |

Five tags + five bookmarks, with visual variants but no meaningless duplication.

## Bonus

| ID range | Count | Status |
|---|---:|---|
| SL_BN_001–005 | 5 | PLANNED |

Planned:
- alphabet / initials;
- number set;
- mini palette card;
- contact sheet;
- quick-start index.

## Production rule

Do not mark an ID APPROVED until the actual exported file exists and passes the B08 checks.

## Research note

Current Canva documentation supports JPEG/PNG uploads under 50 MB and requires the uploader to own or be licensed to use uploaded content. Canva also supports transparent PNG workflows. citeturn0search1turn0search0

Current Etsy shop-image guidance says transparent PNGs used as listing images display their transparent areas as black. Therefore B08 must produce:
1. clean transparent delivery PNGs;
2. separate opaque-background marketing previews for B10/B11. citeturn0search8


## B08 ephemera verification

The ephemera batch was processed through GitHub Actions run `36340334073`.

Verification result:
- 20/20 ephemera SVG masters passed XML preflight.
- 20/20 ephemera PNGs were rendered at 3600×2400.
- PNG transparency QA passed: RGBA/alpha channel present, transparent canvas verified, non-empty artwork verified.
- Filename length QA passed.
- Full repository raster QA passed for 40 journal JPGs + 15 digital-paper JPGs + 20 transparent ephemera PNGs.
- Verification artifact: `b08-asset-delivery-verification`, artifact ID `10938213693`.
- Generated ephemera delivery was committed to main in `937b108`.

A previous run `36340276475` failed because the newly created ephemera masters had not yet been attached to the main branch when the workflow started. This was a repository sequencing issue; the corrected run `36340334073` passed all gates and pushed the delivery successfully.

The 20 ephemera concepts are therefore APPROVED for B08 progress purposes.


## B08 decorative PNG verification

GitHub Actions run `36340693552` completed successfully.

- 20/20 decorative PNG SVG masters passed XML preflight.
- 20/20 decorative PNGs rendered at 3600×3600.
- Transparent PNG QA passed: alpha channel present, transparent canvas verified, non-empty artwork verified.
- Full raster QA passed for 40 journal JPGs + 15 digital-paper JPGs + 20 ephemera PNGs + 20 decorative PNGs.
- Delivery commit: `12f2d77`.

The decorative PNG batch is therefore APPROVED for B08 progress purposes.
