# B07 — Professional Production Pipeline

Дата: 2026-09-27

## Status

**B07 — Production Pipeline: COMPLETE — 100%**

B07 defines the repeatable production system for SKU 001 before any commercial assets are created. B08 must not start until this pipeline is accepted and frozen.

## 1. Production gates

1. **Research gate** — market evidence and product specification are frozen.
2. **Style gate** — visual language is frozen before batch production.
3. **Template gate** — master dimensions and reusable templates are tested.
4. **Naming gate** — every file follows the same naming convention.
5. **Export gate** — source artwork is exported into the exact delivery formats.
6. **Package gate** — final ZIP structure is reproducible and readable.
7. **QA gate** — file count, dimensions, transparency, naming, folder structure and archive integrity are checked.
8. **Listing gate** — only QA-approved files move to B10/B11.

## 2. SKU 001 production target

**SECRET LIBRARY — Dark Academia Journaling Kit**

Target: 90 assets/pages, distributed according to B06.

No filler pages are permitted merely to reach 90. If an asset fails the quality gate, it is replaced rather than counted.

## 3. Visual system

### Core mood
- dark academia;
- antique library;
- scholarly / archival;
- mysterious but usable;
- tactile paper and ink character;
- restrained, coherent decoration.

### Visual rules
- one coherent visual family across every asset type;
- consistent line weight for drawn decorative elements;
- consistent aging/grain treatment;
- controlled contrast so writing areas remain usable;
- decorative assets must remain readable when placed over paper backgrounds;
- no recognizable third-party characters, logos, branded objects or copied artwork;
- no random styles mixed into the same kit.

### Palette
The palette is deliberately limited and documented in the style guide. Every generated or manually created asset must fit the palette or be intentionally marked as an accent.

## 4. Master canvas standards

### Printable journal pages
- US Letter: 2550 × 3300 px
- A4: 2480 × 3508 px
- 300 DPI metadata where the export format supports it.

### Digital paper
- 3600 × 3600 px target minimum.
- JPG for delivery.

### Transparent decorative PNG
- 3000 px or more on the longest side where practical.
- PNG with genuine transparency.
- No accidental white rectangle/background.

These are production standards for this SKU. Marketplace requirements remain separate and must be rechecked before listing.

## 5. Source → export workflow

Every asset follows:

**MASTER SOURCE → WORKING MASTER → DELIVERY EXPORT → VISUAL CHECK → TECHNICAL CHECK → PACKAGE**

Never edit the only delivery file as the master.

### Master principles
- keep editable source files privately;
- preserve clean layer/group organization;
- use predictable document names;
- avoid unnecessary hidden objects and stray elements;
- keep a source-to-delivery mapping.

## 6. Folder architecture

Delivery package:

```text
SECRET_LIBRARY_KIT/
├── 01_JOURNAL_PAGES/
│   ├── US_LETTER/
│   └── A4/
├── 02_DIGITAL_PAPERS/
├── 03_EPHEMERA/
├── 04_DECORATIVE_PNG/
├── 05_TAGS_BOOKMARKS/
├── 06_BONUS/
├── PREVIEWS/
├── README.pdf
└── LICENSE.pdf
```

No empty delivery folders. If a folder is part of the specification, it must contain the promised assets.

## 7. File naming

Canonical format:

`SL_<CATEGORY>_<NNN>_<SHORT_NAME>.<ext>`

Examples:
- `SL_JP_001_LIBRARY_CATALOG.jpg`
- `SL_DP_001_AGED_PARCHMENT.jpg`
- `SL_EP_001_LIBRARY_CARD.png`
- `SL_PNG_001_ANTIQUE_KEY.png`
- `SL_TB_001_RAVEN_BOOKMARK.png`

Rules:
- ASCII characters only for delivery filenames;
- uppercase category codes;
- three-digit sequence numbers;
- no spaces;
- no ambiguous names such as `final2`, `new`, `test`;
- filename describes the asset;
- the same asset keeps the same ID across previews, QA reports and source records.

Etsy currently limits uploaded digital filenames to 70 characters and permits alphanumeric characters, periods, underscores and hyphens; names are visible to buyers and cannot be edited after upload. Therefore the naming standard is intentionally conservative. citeturn0search2turn0search3

## 8. Marketplace delivery constraint

For Etsy, the current official help documentation states:
- up to 5 digital files per instant-download listing;
- maximum 20 MB per uploaded file;
- ZIP is supported;
- uploaded filenames are shown to buyers.

Therefore the product package will be split into delivery ZIPs if the final package exceeds Etsy's per-file limit. The internal product structure stays unchanged. citeturn0search1turn0search2

For Creative Market, current seller documentation states that product files up to 4 GB should be uploaded directly, ZIP is recommended for multiple files, and RAR/7z are not recommended. Creative Market also recommends clear organization and a Read Me/User Guide. citeturn1search0turn1search1turn1search6

**Decision:** build the master package once, then create marketplace-specific delivery packages from it. Never redesign the product around one marketplace's upload UI.

## 9. Preview production

Preview set is part of production, not an afterthought.

Minimum preview system:
1. hero image showing the visual identity;
2. full-kit overview/contact sheet;
3. journal-page close-up;
4. digital-paper close-up;
5. ephemera close-up;
6. transparent PNG showcase;
7. tags/bookmarks showcase;
8. specification/compatibility slide;
9. folder/package preview where useful.

For Creative Market, current guidance permits up to 100 screenshots, requires at least one static screenshot, and recommends screenshots at least 1820 px wide for best results. citeturn1search0

Etsy currently allows up to two listing videos; listing videos can be 3–15 seconds, max 100 MB, with at least 1080 px recommended. Video is optional for B07 and belongs to B10/B11 listing packaging. citeturn0search14

## 10. Compatibility principle

The kit is intentionally built from broadly usable PNG/JPG/PDF assets rather than software-specific editable formats.

Canva currently supports JPEG/PNG/HEIC/HEIF/WebP image uploads under 50 MB and PDF imports up to 300 MB/500 pages. This supports the decision to prioritize standard raster assets and PDF documentation rather than requiring specialized software. citeturn0search0

## 11. Licensing / originality gate

Every commercial asset must be:
- original or created from resources whose commercial license explicitly permits this use;
- free of third-party trademarks and recognizable copyrighted characters;
- not copied from a competitor's product;
- not redistributed from stock/clipart packs as source material where the license forbids resale/redistribution.

Creative Market's current shop-owner guidelines explicitly prohibit third-party resources in products and visible trademarks, and require products to be represented accurately. citeturn1search1

## 12. Reproducibility rule

A second person should be able to understand the delivery package without contacting the creator.

README must state:
- what is included;
- folder map;
- file formats;
- dimensions;
- intended uses;
- basic usage instructions;
- license summary;
- support/contact route;
- version/date.

Creative Market's current best-practice guidance recommends a Read Me/User Guide, clearly named and organized files, and direct product delivery. citeturn1search6

## 13. B07 freeze condition

B07 is considered complete because:
- production gates are defined;
- visual system rules are defined;
- master dimensions are fixed;
- naming convention is fixed;
- folder architecture is fixed;
- export workflow is fixed;
- marketplace delivery constraints are documented;
- preview workflow is defined;
- originality/licensing gate is defined;
- reproducibility/README requirement is defined.

**Next block: B08 — Asset Creation.**
