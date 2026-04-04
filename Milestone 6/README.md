# SwapJoys Platform - Release Notes

## Version 1.5.0

![Release Date](https://img.shields.io/badge/Release%20Date-April%203%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.5.0 delivers the Points System & Balance functionality for the SwapJoys platform. This release enables companies to view their points balance and full transaction history, see point values across the platform, and provides SwapJoys administrators with the ability to manually adjust company point balances with a complete audit trail.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables registered companies to:

- View a comprehensive points and balance dashboard with earned, spent, and pending totals
- Browse complete transaction history with filtering by type, date range, and search
- See point values displayed across marketplace cards, experience details, and booking forms
- Receive automatic balance checks and insufficient points warnings before booking

SwapJoys administrators can now:

- View all companies with their current point balances
- Add or remove points from any company with mandatory reason
- Review a complete audit trail of all admin point adjustments

> This release completes Milestone 6: Points System & Balance (Features 8, 9, 10) and builds on M1 (Foundation), M2 (Company Registration), M3 (Employee Onboarding & Roles), M4 (Experience Creation & Marketplace), and M5 (Booking & QR Verification).

---

## What's New

- Points & Balance dashboard with summary cards and recent transactions
- Full transaction history with type, date range, and search filters
- Transaction detail view with balance before/after tracking
- Points display across marketplace cards, experience detail pages, and booking forms
- SwapJoys admin point adjustment panel with company search
- Admin audit trail with complete adjustment history
- Append-only immutable points ledger architecture
- Employee direct redemption flow for experiences
- Navigation renaming (Marketplace → Experiences, Experiences → My Experiences)
- New SwapJoy logo designed and integrated across platform
- Book a Demo modal on landing page
- Landing page design improvements with custom generated images
- Mobile and tablet responsive design for home screens
- Norwegian/English language toggle updates for M6 screens

---

## New Features

### Feature 8: Simple Fixed-Point System
- Points ledger with append-only immutable architecture
- Transaction types: Welcome Bonus (+50), Booking Deduction (−X), Redemption Credit (+X), Admin Adjustment (+/−X)
- Points displayed on marketplace experience cards
- Points displayed prominently on experience detail pages
- Balance vs. cost comparison on booking request form
- Sufficient/Insufficient points indicator before booking
- Current balance display on dashboard header
- Points per booking shown in My Bookings views
- Transaction history page with full list of all point movements
- Type filter (Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment)
- Date range filter
- Search by experience name or company name
- Combined filters working together
- Pagination (20 transactions per page)
- Transaction detail view with Transaction ID, Date/Time, Type, Experience, Points, Balance Before, Balance After, Other Party, and Notes

### Feature 9: Company Balance Overview
- Points & Balance dashboard page
- Current Balance summary card (large prominent number)
- Points Earned card (total credits)
- Points Spent card (total debits)
- Pending Bookings card (reserved points)
- Balance calculation: Earned − Spent = Current Balance
- Recent Transactions list (last 10 entries)
- Each entry displays: Date, Type icon, Description, Points (+/−), Other Party
- "View All Transactions" link to full history

### Feature 10: Admin Override
- SwapJoys admin point adjustment page
- Company list with current balances
- Search company by name
- Adjust Points form with Add/Remove selection
- Point amount input (positive integer, minimum 1)
- Mandatory reason field (minimum 10 characters)
- Confirmation dialog before processing
- Insufficient balance check for point removal
- Points ledger entry creation (append-only, immutable)
- Admin audit log entry creation
- Success message with new balance display
- Adjustment History page with complete audit trail
- Filter adjustments by company, date range, and type (Add/Remove)
- Adjustment detail view with full information (ID, Admin, Company, Type, Amount, Balance Before/After, Reason, Timestamp)

### Additional Deliverables (Beyond M6 Scope)
- Employee direct redemption flow — employees can directly redeem experiences
- Navigation renaming — Marketplace renamed to Experiences, Experiences renamed to My Experiences, all text and routing updated
- Landing page design improvements with custom generated images
- SwapJoy logo design, generation, editing, and integration across platform (sidebar, landing page, emails, browser tab)
- Book a Demo modal — 10-minute demo booking modal on landing page with form fields and submission flow
- Multi-language support (Norwegian/English) updates for all M6 screens
- Mobile and tablet responsive design — home screens, landing page, dashboard, and sidebar optimized for mobile devices

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (5 phases) | ✅ |
| 2 | Platform Flow Diagram - Points System & Balance | ✅ |
| 3 | Wireframes (7 screens) | ✅ |
| 4 | HTML/CSS Design Templates | ✅ |
| 5 | Backend API - Points Ledger & Balance Calculation | ✅ |
| 6 | Backend API - Transaction History with Filters | ✅ |
| 7 | Backend API - Admin Point Adjustments | ✅ |
| 8 | Backend API - Admin Audit Trail | ✅ |
| 9 | Frontend - Points & Balance Dashboard | ✅ |
| 10 | Frontend - Transaction History & Detail | ✅ |
| 11 | Frontend - Admin Point Adjustments | ✅ |
| 12 | Frontend - Admin Adjustment History & Detail | ✅ |
| 13 | Employee Direct Redemption Flow (Additional) | ✅ |
| 14 | Navigation Renaming Across Platform (Additional) | ✅ |
| 15 | Landing Page Design Improvements (Additional) | ✅ |
| 16 | Logo Design & Integration (Additional) | ✅ |
| 17 | Book a Demo Modal (Additional) | ✅ |
| 18 | Multi-Language Updates for M6 (Additional) | ✅ |
| 19 | Mobile & Tablet Responsive Design (Additional) | ✅ |
| 20 | Server Deployment | ✅ |
| 21 | Release Notes | ✅ |

---

## Screens Delivered

| # | Screen | Type |
|---|--------|------|
| 1 | Points & Balance Dashboard | Protected (Owner/Manager) |
| 2 | Transaction History | Protected (Owner/Manager) |
| 3 | Transaction Detail | Protected (Owner/Manager) |
| 4 | Admin - Point Adjustments | Protected (SwapJoys Admin) |
| 5 | Admin - Adjustment Confirmation | Protected (SwapJoys Admin) |
| 6 | Admin - Adjustment History | Protected (SwapJoys Admin) |
| 7 | Admin - Adjustment Detail | Protected (SwapJoys Admin) |

---

## API Endpoints Delivered

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/points/dashboard` | Points & Balance dashboard data |
| GET | `/api/points/balance` | Current balance with earned/spent totals |
| GET | `/api/points/transactions` | Transaction history with filters and pagination |
| GET | `/api/points/transactions/{id}` | Transaction detail |
| GET | `/api/points/recent` | Recent transactions (last 10) |
| GET | `/api/admin/companies` | Company list with current balances |
| POST | `/api/admin/adjustments` | Create point adjustment |
| GET | `/api/admin/adjustments` | Adjustment history with filters |
| GET | `/api/admin/adjustments/{id}` | Adjustment detail |

---

## Points Ledger Architecture

| Property | Detail |
|----------|--------|
| Storage | Append-only, immutable |
| Entry Fields | Transaction ID, Company ID, Type, Points (+/−), Balance After, Reference ID, Description, Timestamp |
| Integrity | Entries cannot be edited or deleted |
| Balance Calculation | Sum of all ledger entries for company (Earned − Spent = Current) |

---

## Transaction Types

| Type | Icon | Points | Description |
|------|------|--------|-------------|
| Welcome Bonus | 🎁 | +50 | Awarded on company registration |
| Booking Deduction | 📤 | −X | Points deducted when booking is approved |
| Redemption Credit | 📥 | +X | Points credited when ticket is redeemed |
| Admin Adjustment (Credit) | ⚙️ | +X | Admin added points to company |
| Admin Adjustment (Debit) | ⚙️ | −X | Admin removed points from company |

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| View Points Dashboard | ✅ | ✅ | ❌ | ❌ |
| View Transaction History | ✅ | ✅ | ❌ | ❌ |
| View Balance on Dashboard | ✅ | ✅ | ✅ | ❌ |
| View Points on Experiences | ✅ | ✅ | ✅ | ❌ |
| Admin Adjust Points | ❌ | ❌ | ❌ | ✅ |
| Admin View Adjustment History | ❌ | ❌ | ❌ | ✅ |
| Admin View Company Balances | ❌ | ❌ | ❌ | ✅ |

---

## Known Limitations

| Limitation |
|------------|
| QR code generation and camera-based scanning not yet implemented — tickets use 6-character backup codes only |
| Admin dashboard with full company/employee management not yet available (Milestone 7) |
| Usage logs and activity tracking not yet implemented (Milestone 7) |
| Tax documentation module (yearly summary, threshold warnings, CSV export) not yet implemented (Milestones 7-8) |
| Subscription system not yet available (Milestone 8) |

---

## Compatibility Notes

| Note |
|------|
| All M1, M2, M3, M4, and M5 features remain fully compatible |
| Database schema updated with points ledger and admin audit log tables |
| API contracts stable for all delivered features |
| Points ledger uses append-only immutable logging as specified in architecture |
| Navigation naming updated: Marketplace → Experiences, Experiences → My Experiences |
| Admin panel routes are separate from company user routes |

---

<div align="center">

**End of Version 1.5.0 Release Notes**

</div>
