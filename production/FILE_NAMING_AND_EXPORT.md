# B07 — File Naming & Export Standard

Дата: 2026-09-27

## Canonical ID system

Prefix: `SL` = Secret Library

| Code | Category |
|---|---|
| JP | Journal Pages |
| DP | Digital Papers |
| EP | Ephemera |
| PNG | Decorative Transparent PNG |
| TB | Tags / Bookmarks |
| BN | Bonus |

Canonical filename:

`SL_<CODE>_<NNN>_<SHORT_NAME>.<EXT>`

Examples:
- SL_JP_001_LIBRARY_CATALOG.jpg
- SL_JP_001_LIBRARY_CATALOG.pdf
- SL_DP_001_AGED_PARCHMENT.jpg
- SL_EP_001_LIBRARY_CARD.png
- SL_PNG_001_ANTIQUE_KEY.png
- SL_TB_001_RAVEN_BOOKMARK.png
- SL_BN_001_CONTACT_SHEET.pdf

## Export matrix

| Asset | Master | Delivery | Required |
|---|---|---|---|
| Journal page | editable source | JPG + optional PDF | 2550×3300 and 2480×3508 |
| Digital paper | editable source | JPG | ≥3600×3600 target |
| Ephemera | editable source | PNG | transparent where intended |
| Decorative PNG | editable source | PNG | transparent |
| Tag/bookmark | editable source | PNG/JPG according to design | 300 DPI where printable |
| README | source document | PDF | included |
| LICENSE | source document | PDF | included |

## Export checks

Every delivery file is checked for:
- correct extension;
- correct dimensions;
- expected color mode;
- correct transparency state;
- no accidental crop;
- no clipping at edges;
- no white matte on transparent PNG;
- no unreadable tiny text;
- correct sequence number;
- filename compliance;
- successful opening after export.

## Naming rules

- ASCII only;
- uppercase category code;
- three-digit sequence;
- words separated with underscores;
- maximum 70 characters for marketplace upload safety;
- no spaces;
- no duplicate IDs;
- no `FINAL`, `FINAL2`, `NEW`, `TEST` in customer filenames.

Etsy's current documentation confirms the 70-character filename limit and that buyer-visible filenames should be correct before upload. citeturn0search2

## Archive standard

Primary archive:
`SECRET_LIBRARY_KIT_v1.0.zip`

Before marketplace upload:
- extract archive into a clean temporary directory;
- verify every expected folder;
- verify every file opens;
- verify no hidden OS files such as `.DS_Store`;
- verify README and LICENSE are present;
- verify archive can be extracted on a clean environment.

Creative Market currently recommends ZIP for multi-file products and says its editor can inspect ZIP contents; Etsy also supports ZIP as a digital-file type. citeturn1search0turn0search2

## Versioning

- v0.1 = production draft;
- v0.2 = internal QA revision;
- v1.0 = first commercial release;
- v1.1+ = post-launch fixes/additions.

Never silently replace a published product without recording the change.

## B08 handoff

B08 receives:
1. frozen style guide;
2. frozen filename system;
3. frozen export matrix;
4. B06 asset manifest;
5. production gate checklist.

B08 may change individual asset content during creation, but may not change the product architecture without reopening B06/B07.
