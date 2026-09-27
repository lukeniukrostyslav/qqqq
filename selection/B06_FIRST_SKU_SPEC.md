# B06 — First SKU Specification

Дата: 2026-09-27

## SKU 001

**Working title:** SECRET LIBRARY — Dark Academia Journaling Kit

**Audience:** Digital Journaling / Scrapbooking

**Core use cases:**
- digital journaling;
- junk journals;
- scrapbooking;
- digital collage;
- printable journaling;
- bookish / reading journals.

## Why this theme

Current Etsy evidence shows multiple active Dark Academia / Secret Library products:
- Secret Library Junk Journal Kit — 97 reviews; seller shop 31k sales.
- Dark Academia / Grungy Junk Journal product — 30 reviews; seller shop 125.7k sales.
- Dark Academia 137-page kit — current low-ticket product.
- Cursed Library and Librarian's Cabinet products show repeat-purchase behavior and positive reviews.
- A successful seller explicitly offers a "Secret Library Junk Journal Kit" and also related Traveler, Steampunk, Dark Academia and Kitchen kits.

Sources checked 2026-09-27:
- Etsy Secret Library: https://www.etsy.com/listing/1545073193/secret-library-junk-journal-kit
- Etsy Grungy Dark Academia: https://www.etsy.com/listing/1591941075/grungy-dark-academia-junk-journal
- Etsy Dark Academia 137 pages: https://www.etsy.com/listing/4473168119/dark-academia-junk-journal-kit-137-pages
- Etsy Cursed Library: https://www.etsy.com/listing/1887450413/cursed-library-junk-journal-kit

## Why not Autumn as SKU 001

Autumn has strong demand, but current Etsy results are extremely crowded and heavily discounted:
- 5,000+ digital fall scrapbooking kits;
- many visible listings around $0.60–$4;
- multiple products with thousands of reviews.

Autumn remains a future seasonal collection, not the first evergreen SKU.

## Target product size

We deliberately do NOT start with 150–2,000 pages.

SKU 001 target:
**80–100 curated assets/pages total**

Proposed structure:

### 01_JOURNAL_PAGES
20 pages
- lined / writing pages;
- chapter/title pages;
- reading notes;
- library catalogue style pages;
- aged paper backgrounds.

### 02_DIGITAL_PAPERS
15 papers
- parchment;
- old paper;
- dark textured paper;
- subtle book/page patterns.

### 03_EPHEMERA
20 elements
- library cards;
- labels;
- tickets;
- bookmarks;
- envelopes;
- notes;
- stamps;
- catalog cards.

### 04_DECORATIVE_PNG
20 transparent PNG elements
- books;
- keys;
- ink bottles;
- quills;
- candle;
- antique frames;
- botanical accents;
- raven silhouette;
- magnifying glass;
- vintage objects.

### 05_TAGS_BOOKMARKS
10 pieces
- tags;
- bookmarks;
- mini cards.

### 06_BONUS
5 pieces
- alphabet / initials;
- mini palette;
- contact sheet / index.

Target total: **90 assets/pages**.

## File standards

### Printable pages
- US Letter: 8.5 × 11 in
- 2550 × 3300 px
- 300 DPI

### A4 version
- 2480 × 3508 px
- 300 DPI

### Transparent PNG
- minimum 3000 px on the longest side where practical;
- transparent background;
- PNG-24/standard PNG;
- no accidental white background.

### Digital paper
- target 3600 × 3600 px or larger;
- JPG;
- 300 DPI metadata where supported.

## Delivery

ZIP structure:

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

## License

For SKU 001 initial license:
- personal use;
- small-business finished physical/digital end products;
- no resale of source files;
- no redistribution of individual assets;
- no uploading assets to stock/clipart marketplaces;
- no claiming individual assets as original standalone artwork.

Exact legal wording must be reviewed before listing.

## Price hypothesis

Do not copy low-price competitors.

Initial test:
- launch/list price target: **$7.99**
- possible introductory price: **$5.99**
- future premium/bundle target: **$12.99–19.99**

These are hypotheses for testing, not guaranteed market prices.

## QA gate

B06 is complete only when:
- exact file count is confirmed;
- all dimensions are specified;
- both US Letter and A4 plan is confirmed;
- formats are confirmed;
- ZIP structure is confirmed;
- license scope is confirmed;
- preview requirements are confirmed;
- no third-party copyrighted characters/brands are included.

Production does not begin until these checks are passed.
