# SwapJoys Platform MVP

![SwapJoys](https://img.shields.io/badge/SwapJoys-Platform-6366f1)
![Version](https://img.shields.io/badge/version-1.6.0--M7-blue)
![Small Adjustment](https://img.shields.io/badge/latest-1.6.1--Pre--M8-blue)
![Status](https://img.shields.io/badge/status-In%20Development-yellow)
![License](https://img.shields.io/badge/license-Proprietary-red)

> Employee Experience Exchange Platform — A B2B marketplace where companies exchange employee benefits and experiences using a points-based system.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Project Structure](#project-structure)
- [Milestones](#milestones)
- [Installation](#installation)
- [Documentation](#documentation)
- [Team](#team)

---

## Overview

SwapJoys is a B2B platform that enables companies to exchange employee experiences and benefits. Companies can create experiences (dining, wellness, entertainment, etc.) and offer them to employees of other companies through a points-based exchange system.

### Key Concepts

- **Companies** register and manage their employees
- **Experiences** are created and published to a marketplace
- **Points** are used to book experiences from other companies
- **QR Codes** verify and redeem booked experiences
- **Tax Documentation** tracks welfare benefits for Norwegian tax compliance

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React |
| **Backend** | Laravel (PHP) |
| **Database** | MySQL |
| **Authentication** | JWT with Laravel Sanctum |
| **Hosting** | VPS |

### Architecture Principles

- Horizontal Scaling — Stateless services
- Performance — < 2s QR verification, < 300ms API response
- Security — Encryption at rest/transit, RBAC, signed tokens
- Immutable Ledger — Append-only transaction logs
- GDPR Compliance — Data minimization, retention rules

---

## Features

### MVP Scope: 21 Features

#### Module 1: Company & Employee Onboarding (3 Features)
| # | Feature | Description |
|---|---------|-------------|
| 1 | Company Registration | Signup with email verification + 50 welcome points |
| 2 | Employee Onboarding | Manual addition + email invitation system |
| 3 | Role Assignment | Three-tier: Owner / Manager / Employee |

#### Module 2: Experience Marketplace (4 Features)
| # | Feature | Description |
|---|---------|-------------|
| 4 | Create Experience | Title, description, capacity, rules, photo |
| 5 | Browse Experiences | Category + city filters |
| 6 | Request/Book Experience | Booking workflow with approval |
| 7 | QR/Unique Code Verification | Secure verification for redemption |

#### Module 3: Points & Balance (3 Features)
| # | Feature | Description |
|---|---------|-------------|
| 8 | Fixed-Point System | Points for experience exchange |
| 9 | Company Balance Overview | Dashboard showing point status |
| 10 | Admin Override | SwapJoys admin ability to adjust points |

#### Module 4: Admin Tools (3 Features)
| # | Feature | Description |
|---|---------|-------------|
| 11 | SwapJoys Admin Dashboard | Central control panel |
| 12 | Usage Logs | Company & employee activity logs |
| 13 | Experience Status Tracking | Pending / Confirmed / Used |

#### Module 5: Tax Documentation (7 Features)
| # | Feature | Description |
|---|---------|-------------|
| 15 | Estimated Value Field | NOK value per experience |
| 16 | Welfare Classification | Mandatory yes/no tag |
| 17 | Usage Documentation | Complete usage log |
| 18 | Yearly Employee Summary | Annual totals per employee |
| 19 | Threshold Warning | NOK 5,000 limit notification |
| 20 | CSV Tax Export | Downloadable tax report |
| 21 | Legal Disclaimer | Tax responsibility notice |

#### Module 6: Subscription (1 Feature)
| # | Feature | Description |
|---|---------|-------------|
| 14 | Company Membership Payment | 399 NOK/month via Stripe |

---

## Project Structure

```
SwapJoys/
├── Milestone 1/                    # Foundation Setup
│   ├── Documents/
│   │   ├── Release-Notes-M1.md
│   │   ├── Task-Report-M1.pdf
│   │   └── Database-Schema.md
│   ├── Designs/
│   │   ├── Platform-Flow-Diagram.md
│   │   └── UI-Dashboard-Design.html
│   └── Database/
│       └── migrations/
├── Milestone 2/                    # Company Registration
│   ├── Documents/
│   │   ├── Release-Notes-M2.md
│   │   ├── Task-Report-M2.pdf
│   │   └── User-Journey-Map-M2.pdf
│   └── Designs/
│       ├── HTML-CSS-Templates.html
│       └── Landing-Page.html
├── Milestone 3/                    # Employee Onboarding & Roles
│   ├── Deliverables/
│   │   ├── HTMLCSS-design-templates.html
│   │   ├── Platform-Flow-Diagram-Employee-Onboarding.md
│   │   ├── User-Journey-Map.md
│   │   └── Wireframes.md
│   └── Documents/
│       ├── Release-Notes-M3.md
│       └── Task-Report-M3.xlsx
├── Milestone 4/                    # Experience Creation & Marketplace
│   ├── Deliverables/
│   │   ├── HTMLCSS-design-templates.html
│   │   ├── Platform-Flow-Diagram-Experience-Creation-Marketplace.md
│   │   ├── User-Journey-Map.md
│   │   └── Wireframes.md
│   └── Documents/
│       ├── Release-Notes-M4.md
│       └── Task-Report-M4.xlsx
├── Milestone 5/                    # Booking & QR Verification
│   ├── Deliverables/
│   │   ├── HTMLCSS-design-templates.html
│   │   ├── Platform-Flow-Diagram-Booking-QR-Verification.md
│   │   ├── User-Journey-Map.md
│   │   ├── Wireframes.md
│   │   └── Email-Notification-Specs.md
│   └── Documents/
│       ├── Release-Notes-M5.md
│       └── Task-Report-M5.pdf
├── Milestone 6/                    # Points System & Balance
│   ├── Deliverables/
│   │   ├── HTMLCSS-design-templates.html
│   │   ├── Platform-Flow-Diagram-Points-System-Balance.md
│   │   ├── User-Journey-Map.md
│   │   └── Wireframes.md
│   └── Documents/
│       ├── Release-Notes-M6.md
│       └── Task-Report-M6.pdf
├── Milestone 7/                    # Admin Dashboard & Tax Module Part 1
│   ├── Deliverables/
│   │   ├── Htmlcss design templates.html
│   │   ├── Platform Flow Diagram - Admin Dashboard & Tax Module Part 1.md
│   │   ├── User Journey Map.md
│   │   └── Wireframes.md
│   └── Documents/
│       ├── Release-Notes-M7.md
│       └── Task-Report-M7.pdf
├── Milestone 8/                    # Tax Part 2 & Launch (Coming)
│   └── Small Adjustment/           # Pre-M8 Credits Rename & Hero Refresh (v1.6.1)
│       ├── README.md
│       └── Report N008-SA.pdf
└── README.md
```

---

## Milestones

| Milestone | Weeks | Duration | Features | Status |
|-----------|-------|----------|----------|--------|
| **M1** | 1-2 | 2 weeks | Foundation Setup | ✅ Complete |
| **M2** | 3-4 | 2 weeks | Company Registration | ✅ Complete |
| **M3** | 5-6 | 2 weeks | Employee Onboarding, Roles | ✅ Complete |
| **M4** | 7-8 | 2 weeks | Experience Creation, Marketplace | ✅ Complete |
| **M5** | 9-10 | 2 weeks | Booking, QR Verification, Status | ✅ Complete |
| **M6** | 11-12 | 2 weeks | Points System, Balance, Override | ✅ Complete |
| **M7** | 13-14 | 2 weeks | Admin Dashboard, Tax Part 1 | ✅ Complete |
| **M8** | 15-16 | 2 weeks | Tax Part 2, Subscription, Launch | 🔄 Next |
| **M9** | TBD | TBD | Stripe Integration + Final QA | ⏳ Planned |

**Total Timeline:** 16+ weeks | 8+ Milestones | 21 Features

> A pre-Milestone 8 "Small Adjustment" release (v1.6.1) was delivered on June 1, 2026 covering the Points → Credits rename, homepage hero refresh, and translation parity audit. See the "Pre-Milestone 8 — Small Adjustments Delivered" section below for the full list.

---

## Milestone 2 — Additional Delivered

The following features were delivered beyond the original M2 scope:

| Feature | Description |
|---------|-------------|
| Terms & Conditions Page | Legal terms acceptance page |
| Privacy Policy Page | GDPR-compliant privacy information |
| Settings Page | User settings with change password |
| Dashboard Layout | Sidebar navigation structure |
| Protected Routes | Redirect system for unverified users |
| Language Toggle | Norwegian/English language switch |
| Resend Verification | Resend verification email functionality |

---

## Milestone 3 — Additional Delivered

The following features were delivered beyond the original M3 scope:

| Feature | Description |
|---------|-------------|
| New Landing Page Design | Complete redesign with modern layout, hero section, features, CTA |
| 9 AI-Generated Images | Custom images created and integrated into landing page |
| Full Project Color Scheme Change | Updated color palette across all pages to match new landing page |
| Language Toggle (NO/EN) | Norwegian/English language switching across full website |
| Profile in Settings | Added user profile management section in Settings page |

---

## Milestone 4 — Additional Delivered

The following features were delivered beyond the original M4 scope:

| Feature | Description |
|---------|-------------|
| Language Toggle (NO/EN) | Norwegian/English language updates for all M4 screens |

---

## Milestone 5 — Additional Delivered

The following features were delivered beyond the original M5 scope:

| Feature | Description |
|---------|-------------|
| Language Toggle (NO/EN) | Norwegian/English language updates for all M5 screens |

---

## Milestone 6 — Additional Delivered

The following features were delivered beyond the original M6 scope:

| Feature | Description |
|---------|-------------|
| Employee Direct Redemption Flow | Employees can directly redeem experiences, completing full user journey |
| Navigation Renaming | Marketplace renamed to Experiences, Experiences renamed to My Experiences, all text and routing updated |
| Landing Page Design Improvements | Custom generated images and complete landing page design refinements |
| Logo Design & Integration | SwapJoy logo generated, edited, and integrated across platform (sidebar, landing page, emails, browser tab) |
| Book a Demo Modal | 10-minute demo booking modal on landing page with form fields and submission flow |
| Multi-Language Support (NO/EN) | Full English/Norwegian language support updates for all M6 screens |
| Mobile & Tablet Responsive Design | Home screens, landing page, dashboard, and sidebar optimized for mobile phones and tablets |

---

## Milestone 7 — Additional Delivered

The following features were delivered beyond the original M7 scope:

| Feature | Description |
|---------|-------------|
| Multi-Language Support for M7 | Complete English/Norwegian translations for all new M7 pages (Admin Dashboard, Admin Companies, Admin Experiences, Admin Usage Logs with 4 tabs, Tax Reports) |
| VAT Invoice Plan - Design Deliverables | Complete design package for the future VAT/Invoicing module based on client's scope clarification request (10 HTML/CSS interactive screens, wireframes, user journey map, and platform flow diagram covering Register Sale, Use Points, Norwegian-compliant PDF invoice, Invoice Archive, Swap Ledger with VAT, and Accounting Export) |

---

## Pre-Milestone 8 — Small Adjustments Delivered

The following pre-Milestone 8 adjustments were delivered as the v1.6.1 release (June 1, 2026) ahead of full M8 development. All M1-M7 features remain unchanged in behavior:

| Feature | Description |
|---------|-------------|
| Points → Credits Rename (English) | Full UI rename of "Points" / "points" / "Point" / "point" to "Credits" / "credits" / "Credit" / "credit" across all en.json values (100+ value updates across 14 sections); JSON keys preserved for component stability |
| Poeng → Kreditter Rename (Norwegian) | Full Norwegian rename in no.json with linguistically correct compound forms (Kredittsaldo, Kredittkostnad, Kredittjusteringer, Kreditt-transaksjoner, kredittbasert, kampanjekreditter) |
| Homepage Hero Refresh | Updated hero headline ("Swap experiences") and bilingual description copy to reflect the new "local employee experience network" positioning; removed unused titleLight and tagline keys |
| "No Extra Cost" Wording Removal | Removed "at no extra cost" wording from the landing hero and "without additional company cost" / "uten ekstra kostnad" wording from the How It Works Step 3 description in both English and Norwegian |
| Hero Visual Polish | Headline size increased from 46px to 58px, new brand-blue to brand-orange gradient accent underline, description wrapped in a callout box with brand-blue left border and gradient background, refined responsive breakpoints for tablet (<900px), mobile (<600px), and small mobile (<380px) |
| Landing.tsx Hardcoded Text Update | Updated legacy hardcoded copy: "50 Welcome Points" → "50 Welcome Credits", "Balance: 50 Points" → "Balance: 50 Credits", "Your exchange points" → "Your exchange credits", "Available Points" → "Available Credits", "points-based system" → "credits-based system" |
| Translation Parity Audit | Verified en.json and no.json have identical 1,036-key structure (34 sections each), all 922 unique t() references resolve cleanly, zero missing keys, zero hardcoded Points/Poeng text remaining in visible .tsx files |
| Database & Route Stability Preserved | `point_cost` database column, `/points` route paths, and JSON translation key names intentionally preserved to avoid breaking existing bookmarks, data, or component bindings (visual rename only) |
| Production Build & Deployment | Docker frontend image rebuilt and deployed to the production server with the refreshed Credits terminology and hero visuals live |
| Release Notes | Version 1.6.1 release notes published documenting all rename, hero, audit, and removal changes |

---

## Installation

> ⚠️ **Note:** Installation instructions will be updated as development progresses.

### Prerequisites

- PHP 8.1+
- Composer
- Node.js 18+
- MySQL 8.0+
- Git

### Backend Setup (Laravel)

```bash
# Clone repository
git clone https://github.com/RT-SwapJoys/SwapJoys.git
cd SwapJoys

# Install dependencies
composer install

# Configure environment
cp .env.example .env
php artisan key:generate

# Run migrations
php artisan migrate

# Start server
php artisan serve
```

### Frontend Setup (React)

```bash
# Navigate to frontend
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

---

## Documentation

| Document | Description | Location |
|----------|-------------|----------|
| Release Notes | Milestone completion summaries | `/Milestone X/Documents/` |
| Task Reports | Detailed work breakdown | `/Milestone X/Documents/` |
| Flow Diagrams | User journey maps | `/Milestone X/Designs/` |
| UI Designs | HTML/CSS mockups | `/Milestone X/Designs/` |
| Database Schema | ERD and migrations | `/Milestone X/Database/` |

---

## License

This project is proprietary software developed for SwapJoys. All rights reserved.

**© 2026 SwapJoys. Developed by Rebing Tech.**

---
