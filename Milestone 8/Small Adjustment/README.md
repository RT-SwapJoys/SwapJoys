# SwapJoys Platform - Release Notes

## Version 1.6.1

![Release Date](https://img.shields.io/badge/Release%20Date-June%201%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.6.1 is a pre-Milestone 8 small adjustment release. Following a strategic business model change confirmed by the client on Discord, the platform's user-facing terminology has been refreshed from "Points" to "Credits" in both English and Norwegian, the homepage hero has been updated to reflect the new "local employee experience network" positioning, and the "no extra cost" wording has been removed per the client's request. All Milestone 1 through Milestone 7 features remain fully functional and unchanged in behavior; this release is a visual and copy-level refresh only.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a credits-based marketplace.

---

## Platform Summary

The platform now presents to all users a consistent, refreshed business language:

- All user-facing screens display "Credits" instead of "Points" in English
- All Norwegian screens display "Kreditter" (or singular compounds such as "Kredittsaldo", "Kredittkostnad") instead of "Poeng"
- The landing page hero communicates the new positioning: SwapJoy connects local businesses through employee experiences offered during quieter periods
- The "no extra cost" wording has been removed from the landing hero and from the "How It Works" Step 3 description in both languages
- The legacy Landing.tsx component now displays "50 Welcome Credits" and "Available Credits" instead of the previous Points wording

> This release adjusts the visual and language layer ahead of full Milestone 8 development. It builds on M1 through M7 without changing any business logic.

---

## What's New

- Full UI rename of "Points" to "Credits" in English (en.json)
- Full UI rename of "Poeng" to "Kreditter" in Norwegian (no.json) with linguistically correct compound forms
- Updated homepage hero copy in both languages to reflect the new "local employee experience network" positioning
- Removal of "at no extra cost" wording from the landing hero (English + Norwegian)
- Removal of "without additional company cost" / "uten ekstra kostnad" wording from the How It Works Step 3 description in both languages
- Updated hardcoded copy in the legacy Landing.tsx component for consistent language
- Refreshed hero visual hierarchy: enlarged headline, gradient accent underline, and a callout-styled description block
- Translation parity audit confirming both en.json and no.json have identical 1,036-key structure with all 922 t() references resolving cleanly

---

## Changes Included

### Language & Terminology Rename
- "Points" / "points" / "Point" / "point" replaced with "Credits" / "credits" / "Credit" / "credit" across all en.json values
- "Poeng" / "poeng" replaced with "Kreditter" / "kreditter" across all no.json values, including compound nouns: Kredittsaldo, Kredittkostnad, Kredittjusteringer, Kreditt-transaksjoner, kredittbasert, kampanjekreditter
- 14 sections updated: Layout, Dashboard, Email Verified, Company Profile, Settings, Marketplace, Experiences, Terms & Conditions, Bookings, Points (now Credits) section, Admin Dashboard, Usage Logs, Admin Experiences
- All JSON keys preserved unchanged for component stability (no breaking changes; zero .tsx code edits required for the rename)
- Database column `point_cost` intentionally preserved for backend stability; rename is visual only

### Homepage Hero Refresh
- Hero headline updated: "Swap experiences"
- Hero description updated to reflect new business positioning (EN + NO)
- Unused `titleLight` and `tagline` keys removed from both translation files
- "no extra cost" wording removed from `hero.titleLight` (now removed entirely)

### How It Works Section
- Step 3 description updated in both languages to remove the "without additional company cost" / "uten ekstra kostnad" wording, replaced with positive framing about enjoying experiences from local businesses

### Hardcoded Text Update - Landing.tsx
- "50 Welcome Points" → "50 Welcome Credits"
- "Balance: 50 Points" → "Balance: 50 Credits"
- "Your exchange points" → "Your exchange credits"
- "Available Points" → "Available Credits"
- "points-based system" → "credits-based system"

### Hero Visual Polish
- Headline size increased from 46px to 58px
- New gradient accent underline (brand-blue to brand-orange) under the hero headline
- Description wrapped in a callout box with brand-blue left border and subtle gradient background
- Responsive breakpoints refined for tablet (<900px), mobile (<600px), and small mobile (<380px)

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | en.json - Points → Credits rename (100+ value updates across 14 sections) | ✅ |
| 2 | no.json - Poeng → Kreditter rename with Norwegian compound forms | ✅ |
| 3 | Landing.tsx - hardcoded "Points" text update (5 occurrences) | ✅ |
| 4 | Homepage hero copy refresh (EN + NO) | ✅ |
| 5 | Removal of "no extra cost" wording from hero and step3Desc (EN + NO) | ✅ |
| 6 | Removal of unused hero.titleLight and hero.tagline translation keys | ✅ |
| 7 | Hero visual polish (typography, accent underline, callout description, responsive) | ✅ |
| 8 | Translation parity audit (1,036 keys ↔ 1,036 keys, identical structure) | ✅ |
| 9 | t() reference resolution check (922 unique references, zero missing keys) | ✅ |
| 10 | Cross-page language QA in English and Norwegian | ✅ |
| 11 | Hardcoded text sweep across all .tsx files | ✅ |
| 12 | Production build verification (Docker frontend image) | ✅ |
| 13 | Server Deployment | ✅ |
| 14 | Release Notes | ✅ |

---

## Pages Updated

| # | Page | Change |
|---|------|--------|
| 1 | Landing Page | Hero refreshed, "no extra cost" removed, Step 3 description updated, legacy hardcoded Points → Credits |
| 2 | Dashboard | Credits Balance, Monthly Credits Earned, Monthly Credits Spent labels |
| 3 | Credits & Balance (formerly Points & Balance) | Page title and all section labels renamed |
| 4 | Transaction History | Credits column, Credit Adjustments references |
| 5 | Marketplace | "X Credits" display on every experience card |
| 6 | Experience Detail | Credit Cost label, validation messages |
| 7 | Experience Form (Create / Edit) | Credit Cost field label and hint text |
| 8 | My Bookings | Credits Deducted, Need more credits, Insufficient credits balance |
| 9 | Company Profile | Credits Balance display |
| 10 | Settings | Credits Balance info field |
| 11 | Email Verified Welcome Page | Credits label |
| 12 | Terms & Conditions | Section 5 "Credits and Balance", Section 1 and Section 7 references updated |
| 13 | Admin Dashboard | Credits in Circulation, Credits by Company labels |
| 14 | Admin Usage Logs | Credits column in Transaction Log tab |
| 15 | Admin Companies | Credits Balance reference |
| 16 | Admin Experiences | Credits column |

---

## Translation Audit Results

| Metric | Result |
|--------|--------|
| en.json total keys | 1,036 (34 sections) |
| no.json total keys | 1,036 (34 sections) |
| Keys missing from no.json | 0 |
| Keys extra in no.json | 0 |
| Unique t() references across React codebase | 922 |
| t() references pointing to missing keys | 0 |
| Hardcoded Points/Poeng text in .tsx files (visible) | 0 |
| Routes containing /points (intentionally preserved for stability) | 3 |

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| View Credits Balance (Dashboard) | ✅ | ✅ | ✅ | ✅ |
| Access Credits & Balance page | ✅ | ✅ | ❌ | ❌ |
| View Credit Cost on Experiences | ✅ | ✅ | ✅ | ✅ |
| Admin Credit Adjustments | ❌ | ❌ | ❌ | ✅ |
| View Credits in Circulation (Admin Dashboard) | ❌ | ❌ | ❌ | ✅ |

> All access rules from M1-M7 remain unchanged. This release does not introduce new permissions.

---

## Known Limitations

| Limitation |
|------------|
| The database column name `point_cost` is intentionally preserved and not renamed; this is a visual rename only and does not affect data integrity |
| Internal URL route paths (`/points`, `/points/transactions`, `/admin/points`) are intentionally preserved to avoid breaking existing bookmarks and links |
| JSON translation key names (e.g. `points.pageTitle`, `pointCost`) are preserved unchanged to maintain component stability; only the displayed values are updated |
| Yearly employee summary remains scheduled for Milestone 8 |
| NOK 4,000 threshold warning per employee remains scheduled for Milestone 8 |
| CSV tax export for employee welfare remains scheduled for Milestone 8 |
| Subscription module remains scheduled for Milestone 8 |

---

## Compatibility Notes

| Note |
|------|
| All M1-M7 features remain fully compatible |
| Database schema unchanged - no migration required |
| `points_ledger` table and `point_cost` column on `experiences` table are unchanged |
| All API contracts remain stable; no endpoint changes |
| All component files (.tsx) require no source changes for the rename - translation values are read at runtime via t() |
| Language toggle continues to work consistently across all screens |
| Norwegian translations use linguistically correct compound noun forms |

---

<div align="center">

**End of Version 1.6.1 Release Notes**

</div>
