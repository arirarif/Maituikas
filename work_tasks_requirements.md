# Work Tasks & Requirements Tracking Log

## Project Overview

| Field             | Details                                                    |
|-------------------|------------------------------------------------------------|
| **Project**       | WooCommerce Laptop Ecommerce Store                         |
| **Client**        | maituikas (Mait) - Estonia                                 |
| **Developer**     | Tonni (A / Me)                                             |
| **Domain**        | arvutipoisid.mtshop.ee                                     |
| **Price**         | $350                                                       |
| **Timeline**      | 12 days delivery (extended by client - no deadline pressure)|
| **Start Date**    | Jan 08, 2026                                               |
| **Source Data**    | x-kom.pl (Polish laptop store)                             |
| **Reference Design** | oixio.ee + mts.ee color scheme                          |
| **JSON Source**   | https://mts.ee/storage/export/laptop_products_cleaned.json |
| **Data Size**     | ~300-400 laptops, ~3000-4000 with variations               |

---

## Access Credentials Provided

| Service    | Details                                      |
|------------|----------------------------------------------|
| **FTP**    | host: arvutipoisid.mtshop.ee                 |
| **DB**     | host: d91289.mysql.zonevs.eu, db: d91289_arvutipoisid |
| **WP Admin** | https://arvutipoisid.mtshop.ee/wp-admin   |

---

## Requirements & Tasks

### 1. Full WooCommerce Store Setup

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 1.1 | Install fresh WordPress + WooCommerce                          | DONE        | Jan 08           |
| 1.2 | Layout similar to oixio.ee/et/e-pood/sulearvutid               | IN PROGRESS | Jan 08, Jan 23   |
| 1.3 | Color scheme: dark grey & green from mts.ee                     | IN PROGRESS | Jan 08, Jan 23   |
| 1.4 | Clean, fast, scalable WooCommerce configuration                 | IN PROGRESS | Jan 08           |
| 1.5 | Easy-to-manage backend for admins                               | IN PROGRESS | Jan 08           |
| 1.6 | Premium theme & plugins (provided at no extra cost)             | DONE        | Jan 02           |

### 2. Automated Product Sync via JSON (Core Feature)

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 2.1 | Custom PHP import script (no 3rd party plugins)                 | DONE        | Jan 08           |
| 2.2 | Read data from JSON URL                                         | DONE        | Jan 11           |
| 2.3 | Auto add new products                                           | DONE        | Jan 11           |
| 2.4 | Auto update existing products (price, stock, config)            | DONE        | Feb 04-05        |
| 2.5 | Auto remove deleted products (not in JSON anymore)              | DONE        | Jan 08           |
| 2.6 | Sync prices                                                     | DONE        | Jan 08           |
| 2.7 | Sync stock availability                                         | DONE        | Jan 08           |
| 2.8 | Handle all attributes & variations correctly                    | DONE        | Feb 05           |
| 2.9 | Cron-compatible execution (every 15-30 min)                     | DONE        | Jan 08           |
| 2.10 | No duplication or conflicts on re-run                          | FIXED       | Jan 27 (dup entry bug fixed) |
| 2.11 | Custom admin UI for sync (manual run, schedule, delete)        | DONE        | Jan 11           |
| 2.12 | Variable products import (AlternativeProducts from JSON)       | DONE        | Feb 05           |
| 2.13 | SKU assignment for all products including out-of-stock          | PENDING     | Feb 04           |
| 2.14 | Product title = Producer + Name (e.g. "MSI Katana 17...")      | PARTIALLY FIXED | Feb 05 (WhatsApp) |
| 2.15 | Producer name MUST be prepended to product title               | PENDING     | Feb 05 (WhatsApp) |
| 2.16 | Delete old attributes & re-import (doubled attributes issue)   | PENDING     | Feb 05 (WhatsApp) |
| 2.17 | Translated attributes in JSON - must be re-imported            | PENDING     | Feb 05 (WhatsApp) |
| 2.18 | Fix stock qty=1 showing "out of stock" (meta saving bug)       | OPEN BUG    | Feb 06 (WhatsApp) |
| 2.19 | SKU on product page replaced by WooCommerce product ID         | PENDING     | Feb 05 (WhatsApp) |
| 2.20 | Product count in filters must match actual products/variations  | PENDING     | Feb 08 (WhatsApp) |

### 3. Multilingual Store (EE, EN, FI)

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 3.1 | WPML or Polylang setup                                          | PENDING     | Jan 08           |
| 3.2 | EE as default language                                          | PENDING     | Feb 02           |
| 3.3 | EN language support                                             | PENDING     | Feb 02           |
| 3.4 | FI language support                                             | PENDING     | Feb 02           |
| 3.5 | Products, attributes, categories translatable                   | PENDING     | Jan 08           |
| 3.6 | JSON-driven products compatible with multilingual               | PENDING     | Jan 08           |
| 3.7 | Clean language switching & SEO-friendly URLs                    | PENDING     | Jan 08           |

### 4. Product Variations Display

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 4.1 | Variations import from AlternativeProducts in JSON              | DONE        | Feb 05           |
| 4.2 | Default variations pre-selected (not empty fields)              | PENDING     | Jan 24           |
| 4.3 | Buttons layout for <=3 variations (like RAM)                    | PENDING     | Jan 24           |
| 4.4 | Dropdown layout for >3 variations (like SSD)                    | PENDING     | Jan 24           |
| 4.5 | Price changes dynamically with variation selection              | DONE        | Jan 21           |

### 5. Filters (Left Sidebar)

**CRITICAL (Feb 08): Client reports ALL filters are WRONG - attributes are mapped to wrong filters!**

#### 5A. Main Filters (1st level - UNCOLLAPSED by default)

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 5.1 | Price slider filter                                             | WRONG       | Feb 05, Feb 08   |
| 5.2 | Producer / Manufacturer filter (must include Apple, Microsoft!) | WRONG       | Feb 05, Feb 08   |
| 5.3 | Screen size filter (JSON id: "000350000000")                    | PENDING     | Feb 05           |
| 5.4 | Touchscreen filter (JSON id: "072890000000")                    | PENDING     | Feb 05           |
| 5.5 | Screen refresh rate filter (JSON id: "060260000000")            | PENDING     | Feb 05           |
| 5.6 | Processor / CPU filter (JSON id: "000220000000_brand/series/name") | WRONG    | Feb 05, Feb 08   |
| 5.7 | RAM filter (JSON id: "000580000000")                            | WRONG       | Feb 05, Feb 08   |
| 5.8 | Maximum Supported RAM filter (JSON id: "000640000000")          | PENDING     | Feb 05           |
| 5.9 | Number of Memory Slots Total/Free (JSON id: "000310000000")    | PENDING     | Feb 05           |
| 5.10 | SSD filter (JSON id: "000320072378")                           | PENDING     | Feb 05           |
| 5.11 | Operating System filter (JSON id: "000440000000")              | WRONG       | Feb 05, Feb 08   |

#### 5B. Secondary Filters (from attributes file - COLLAPSED by default)

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 5.12 | All remaining attributes as collapsed filters                  | PENDING     | Feb 05           |

#### 5C. Filter Design & Behavior

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 5.13 | Checkbox-style selection boxes (not plain text)                | PENDING     | Feb 03           |
| 5.14 | Main filters uncollapsed by default                            | PENDING     | Feb 03, Feb 05   |
| 5.15 | Other filters collapsed by default                             | PENDING     | Feb 05           |
| 5.16 | "Select all" option per filter block                           | PENDING     | Feb 03           |
| 5.17 | Logical sorting (small to big: 4GB, 8GB, 16GB...)             | PENDING     | Feb 03           |
| 5.18 | Reduce spacing between filter blocks                           | PENDING     | Feb 03           |
| 5.19 | Correct attribute mapping from JSON features (BY JSON ID!)     | WRONG       | Feb 03-08        |
| 5.20 | Product count in filters must match real product/variation count| WRONG       | Feb 08           |

**Feb 08 Specific Errors Reported by Client:**
- CPU filter shows "Yes or No" instead of processor names
- Hard Drive filter shows "120hz" (refresh rate data, not HDD data!)
- Operating System filter shows "16GB" (RAM data, not OS data!)
- GPU filter shows "16 GB" (RAM data, not GPU data!)
- Manufacturer filter missing Apple and Microsoft
- Product counts in filters don't match actual products

### 6. Design & Layout

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 6.1 | No separate landing page                                        | DONE        | Jan 09           |
| 6.2 | Clean landing page: laptops + filters visible immediately       | IN PROGRESS | Jan 17           |
| 6.3 | Remove all banners, best offers, popular categories             | IN PROGRESS | Jan 17, Feb 01   |
| 6.4 | Single category: "Laptops" (not 3 separate)                    | DONE        | Jan 11           |
| 6.5 | Bigger logo                                                     | PENDING     | Jan 18           |
| 6.6 | Maintenance mode enabled during development                     | DONE        | Jan 20           |
| 6.7 | Currency set to EUR                                             | DONE        | Feb 01           |
| 6.8 | Product specification table (all unique attributes from JSON)   | PENDING     | Jan 09           |
| 6.9 | Description tab: hide if no description, show only Specification| PENDING     | Feb 05 (WhatsApp) |
| 6.10 | If description exists, show both Description + Specification   | PENDING     | Feb 05 (WhatsApp) |

### 7. Menu & Pages

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 7.1 | Menu: Shop                                                      | DONE        | Jan 18-20        |
| 7.2 | Menu: About Us                                                  | DONE        | Jan 18-20        |
| 7.3 | Menu: Payment by Installments                                   | DONE        | Jan 18-20        |
| 7.4 | Menu: Terms and Conditions of Sales and Guarantee               | DONE        | Jan 18-20        |
| 7.5 | Menu: Purchase and Delivery                                     | DONE        | Jan 18-20        |
| 7.6 | Menu: Privacy Policy (was redirecting to promotions - fix)      | FIXED       | Jan 20           |
| 7.7 | Menu: Contact Us                                                | DONE        | Jan 18-20        |
| 7.8 | Page content copied from mts.ee (all 3 languages)              | PENDING     | Jan 20           |

### 8. Additional Deliverables

| # | Task                                                              | Status      | Date Discussed   |
|---|-------------------------------------------------------------------|-------------|------------------|
| 8.1 | Video tutorial for product/variation management                 | PENDING     | Jan 08           |
| 8.2 | Documentation / guidance                                        | PENDING     | Jan 08           |
| 8.3 | Long-term maintenance support                                   | OFFERED     | Jan 02           |

---

## Issues Encountered & Resolved

| # | Issue                                                    | Status   | Date        |
|---|----------------------------------------------------------|----------|-------------|
| 1 | FTP access not working (IP whitelisting needed)          | RESOLVED | Jan 08-11   |
| 2 | FileZilla not installing on developer devices            | RESOLVED | Jan 11      |
| 3 | DB remote access blocked                                 | RESOLVED | Jan 11      |
| 4 | Product pages not opening (404)                          | RESOLVED | Jan 17      |
| 5 | 500 Internal Server Error                                | RESOLVED | Jan 24-27   |
| 6 | DB duplicate entry error during attribute import         | RESOLVED | Jan 27      |
| 7 | WooCommerce update conflicted with custom sync plugin    | RESOLVED | Feb 03-04   |
| 8 | Malware found on website (hidden in product URL)         | RESOLVED | Feb 05      |
| 9 | Sync plugin temporarily not working / button missing     | RESOLVED | Feb 03-04   |
| 10 | Privacy Policy page redirecting to Promotions           | RESOLVED | Jan 20      |
| 11 | Out-of-stock items missing SKUs                         | OPEN     | Feb 04      |
| 12 | Filter spacing too large                                | OPEN     | Feb 03      |
| 13 | Manufacturer/Brand filter missing Apple & Microsoft     | OPEN     | Feb 03, Feb 08 |
| 14 | Filter sorting random instead of logical                | OPEN     | Feb 03      |
| 15 | Product title missing Producer name prefix              | OPEN     | Feb 05 (WhatsApp) |
| 16 | Doubled attributes - need full delete & re-import       | OPEN     | Feb 05 (WhatsApp) |
| 17 | Stock qty=1 shows "out of stock" (meta saving bug)      | OPEN     | Feb 06 (WhatsApp) |
| 18 | Elementor plugin conflict (Fatal error: get_ally...)    | OPEN     | Feb 06 (WhatsApp) |
| 19 | ALL filters mapped to WRONG attributes (Feb 08)        | OPEN     | Feb 08 (WhatsApp) |
| 20 | CPU filter shows "Yes/No" instead of processor names   | OPEN     | Feb 08 (WhatsApp) |
| 21 | Hard Drive filter shows "120hz" (wrong data)            | OPEN     | Feb 08 (WhatsApp) |
| 22 | Operating System filter shows "16GB" (wrong data)       | OPEN     | Feb 08 (WhatsApp) |
| 23 | GPU filter shows "16 GB" (wrong data)                   | OPEN     | Feb 08 (WhatsApp) |
| 24 | Filter product counts don't match actual products       | OPEN     | Feb 08 (WhatsApp) |

---

## Communication Timeline Summary

| Date       | Key Event                                                        |
|------------|------------------------------------------------------------------|
| Jan 02     | Initial project inquiry from client                              |
| Jan 08     | Project started, credentials shared, order accepted ($350)       |
| Jan 09     | JSON structure discussed, sync approach agreed                   |
| Jan 11     | FTP access resolved, initial product import (3000+ products)     |
| Jan 13-14  | Plugin confirmed working, design work started                    |
| Jan 17     | Design issues: product pages not opening, landing page feedback  |
| Jan 18     | Menu items, category, logo size discussed                        |
| Jan 20     | Pages & menus added, maintenance mode enabled, content from mts.ee |
| Jan 21     | Product variations (AlternativeProducts) structure explained     |
| Jan 22     | Server cache issues, plugin conflict                             |
| Jan 24     | Variable products import working, client confirmed "GOOD JOB!"  |
| Jan 27     | 500 error investigated, duplicate entry bug, server logs shared  |
| Jan 30     | Database errors cleaned, design work resumed                     |
| Feb 01     | Design feedback: remove clutter, add filters, switch to EUR      |
| Feb 02     | Multilingual (EE/EN/FI) discussed, sync failing after JSON update|
| Feb 03     | Filter details discussed (attributes, sorting, checkboxes, spacing)|
| Feb 04     | Sync fixed, attributes updated by client, 1 variable product found|
| Feb 05     | Variations import confirmed working, malware removed, WhatsApp comms started |
| Feb 05     | (WhatsApp) Product title fix, filter IDs specified, attribute re-import needed |
| Feb 06     | (WhatsApp) Stock qty=1 bug reported, Elementor plugin conflict, client asks for action plan |
| Feb 08     | (WhatsApp) ALL FILTERS WRONG - every filter mapped to wrong attribute data |
| Feb 08     | Client frustrated: "basically every filter is wrong", "do you even check your work?" |
| Feb 08     | Client requests task log: "do you write somewhere what I have asked you to do?" |

---

## Overall Progress Summary

| Category                    | Progress          |
|-----------------------------|-------------------|
| WooCommerce Store Setup     | ~70% DONE         |
| JSON Sync Plugin            | ~80% DONE (bugs)  |
| Product Variations Import   | ~85% DONE         |
| Filters Implementation      | ~10% (ALL WRONG)  |
| Design & Layout             | ~40% DONE         |
| Multilingual (EE/EN/FI)     | NOT STARTED       |
| Menu & Pages                | ~80% DONE         |
| Page Content (from mts.ee)  | NOT STARTED       |
| Video Tutorial              | NOT STARTED       |

---

## URGENT / Next Priority Actions (as of Feb 08)

**CRITICAL - Fix immediately:**
1. FIX ALL FILTERS - every filter is mapped to wrong attribute data (CPU shows Yes/No, HDD shows 120hz, OS shows 16GB, GPU shows 16GB)
2. Use correct JSON feature IDs to map filters (IDs provided by client Feb 05)
3. Add missing producers to Manufacturer filter (Apple, Microsoft, etc.)
4. Fix product counts in filters to match actual products/variations
5. Fix stock quantity=1 showing "out of stock" (meta saving bug in import script)
6. Delete doubled attributes and re-import with translated attributes from updated JSON

**HIGH PRIORITY:**
7. Product title must include Producer prefix (e.g. "Dell 14 Core 7 150U/16GB/512/Win11")
8. SKU on product page replaced by WooCommerce product ID
9. Description tab: hide if empty, show only Specification; if description exists show both
10. Fix Elementor plugin conflict (Fatal error)
11. Filter design: checkboxes, spacing, sorting, expand/collapse behavior

**MEDIUM PRIORITY:**
12. Finalize design to match oixio.ee layout with mts.ee colors
13. Default variation pre-selection on product pages
14. Variation display: buttons (<=3) vs dropdown (>3)
15. Product specification table on product pages

**PENDING (after above done):**
16. Multilingual setup (EE, EN, FI)
17. Copy page content from mts.ee in all 3 languages
18. SKU fix for out-of-stock products
19. Final testing of cron sync (add/update/delete cycle)
20. Video tutorial for client

---

## Client Sentiment Notes

| Date   | Sentiment                                                                    |
|--------|------------------------------------------------------------------------------|
| Jan 24 | Positive: "You are doing a good job! I am grateful!" / "GOOD JOB!"          |
| Jan 20 | Supportive: "Take as long as you need to finish"                             |
| Feb 06 | Concerned: "can you increase your productivity?"                             |
| Feb 06 | Questioning: "do you know anything about computers?"                         |
| Feb 08 | Frustrated: "basically every filter is wrong" / "do you even check your work?" |
| Feb 08 | Requesting accountability: "do you write somewhere what I have asked you to do?" |
