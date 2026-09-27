# Audience Comparison — 2026-09-27

## Decision

Primary audience for the first product validation:

**DIGITAL JOURNALING / SCRAPBOOKING**

## Evidence

Etsy's Scrapbook Kits Digital category shows 5,000+ items. Visible listings include:
- Bluebird Rose Mystery Victorian Home Scrap Pack — $4.59, 137.1k reviews.
- Peculiar Pages Printable Junk Journal Kit — $5.99, 15.9k reviews.
- 4,500+ Mega Fussy Cut Bundle — $3.14, 4.7k reviews.
- Junk Journal Paper Pack — $3.14, 22.8k reviews.
- Blue Bliss Junk Journal Ephemera — $2.79, 42.5k reviews.
- September Digital GoodNotes Planner Bundle — about $24, 1.9k reviews.

Etsy's Best Selling Digital Printable Scrapbook page also shows products such as:
- Pumpkin Farm collection — about $11.39 sale.
- Heirloom Scrapbook Junk Journal Kit — $5.84, 854 reviews.
- Christmas Junk Journal Kit — $4.45, 3.6k reviews.
- Fruit Fairy Paper Dolls / ephemera — $1.80, 2.6k reviews.
- Vintage Junk Journal Kit Bundle — $6.57, 396 reviews.
- Sarcastic Sticker Bundle — $1.87, 3.9k reviews.
- 100 Groovy Checkerboard digital scrapbooking paper — $1.32, 24.1k reviews.

A current Etsy listing for a 2,333+ page vintage junk journal bundle states 16 themed kits, A4 + US Letter, 300 DPI and commercial license; the shop page reports 3k sales after about one year. This demonstrates the strength of the bundle model, but this scale is not our required starting point.

Creative Market examples are closely aligned with our proposed architecture. Orchard Days is a 170-file scrapbook kit containing notebook papers, solid papers, torn papers, patterned papers, overlays, decorative elements and washi tape. Woven Memories combines PNG transparent elements, JPEG backgrounds, 300 DPI assets, alphabet tiles, botanical elements, washi tape and decorative objects.

## Comparison

### Digital Journaling / Scrapbooking
- Demand signals: strong
- Production speed: high
- Faceless: yes
- Server/VPS: no
- One-time sale: yes
- Series potential: very high
- Bundle potential: very high
- Technical complexity: low/medium
- IP risk: manageable with original assets
- Price range observed: low-ticket kits through approximately $10–25 larger curated products

### Printable / Planner
Strong demand and prices around $10–25 for larger kits, but compatibility with specific planner formats/apps creates extra QA and maintenance.

### Cricut / Crafting
Strong demand, but visible Etsy pricing is often around $1–5 and competition is intense. IP risk is also higher because some popular listings rely on brands/characters.

### Small Business Designers
Higher price potential, but significantly higher expectations for technical quality, commercial licensing and professional design standards.

## Decision rationale

Digital Journaling / Scrapbooking provides the best starting combination for this project:
- strong demand signals;
- multiple price bands;
- simple raster formats;
- high content reusability;
- high serial-production potential;
- natural bundle model;
- no infrastructure requirement.

This is a controlled validation decision, not a guarantee of sales.

## Next block

B06 — First SKU Specification:
1. exact theme;
2. exact asset count;
3. dimensions;
4. formats;
5. DPI;
6. ZIP structure;
7. license;
8. previews;
9. title;
10. price test.
