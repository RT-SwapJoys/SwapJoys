# SwapJoys Platform - Release Notes

## Version 1.6.0

![Release Date](https://img.shields.io/badge/Release%20Date-April%2017%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.6.0 delivers the Admin Dashboard and Tax Module Part 1 for the SwapJoys platform. This release enables SwapJoys administrators to monitor the entire platform through a central dashboard, manage all registered companies, oversee every experience, and analyze activity through comprehensive usage logs. Company owners and managers can now access Tax Reports for employee welfare documentation. Estimated NOK value and welfare classification are now surfaced consistently across the platform for tax compliance.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables SwapJoys administrators to:

- View platform-wide metrics at a glance (companies, employees, experiences, redemptions, points)
- Monitor recent platform activity across all companies
- Manage all registered companies with detail views, statistics, and employee lists
- Activate or suspend companies directly from the admin panel
- Browse all experiences across the platform with NOK value and welfare tag visible
- Filter experiences by category and city for faster discovery
- Analyze usage through four dedicated log tabs: Transaction, Redemption, Company Activity, and Employee Activity
- Export each log to professional Excel (XLSX) format with SwapJoys branding and summary totals

Company owners and managers can now:

- Access the Tax Reports page for employee experience usage documentation
- View every redemption with employee, experience, host company, NOK value, and welfare tag
- Filter tax reports by employee, welfare status, and date range
- See running totals of Total NOK Value, Welfare Benefits Total, and Total Redemptions
- Rely on automatic usage logging: each ticket redemption now creates an immutable log entry

> This release completes Milestone 7: Admin Dashboard & Tax Module Part 1 (Features 11, 12, 15, 16, 17) and builds on M1 through M6.

---

## What's New

- Complete SwapJoys Admin Dashboard with platform metrics and recent activity
- Admin Company management with detail views and activate/suspend controls
- Admin Experience management with NOK value and welfare tag visible on every row
- Admin Usage Logs with four tabs and advanced filters
- Excel (XLSX) export for all four admin log types with professional formatting
- Automatic usage log creation on every ticket redemption for tax documentation
- Tax Reports page for company owners and managers
- Estimated value (NOK) consistently displayed on experiences, tickets, and all relevant logs
- Welfare classification badge consistently displayed across platform
- Norwegian/English translations for all new M7 screens

---

## New Features

### Feature 11: SwapJoys Admin Dashboard
- Admin Dashboard overview page with 5 platform metric cards (Total Companies, Total Employees, Active Experiences, Total Redemptions, Points in Circulation)
- Platform Growth chart showing companies and employees registered over the last 6 months
- Monthly Redemptions chart showing redemption volume per month
- Points by Company chart showing point distribution across top companies
- Recent Activity feed showing the latest 10 platform events with date, event type, and company
- Admin Companies page with list, search, pagination, and detail view
- Company detail view with company information card, statistics card, and employee list
- Activate / Suspend company status toggle with confirmation
- Admin Experiences page with list, search, category filter, city filter, and pagination
- Experience detail view with photo, full details, NOK value badge, and welfare badge
- Admin-dedicated sidebar section with Dashboard, Companies, Experiences, Usage Logs, and Point Adjustments

### Feature 12: Company & Employee Usage Logs
- Transaction Log tab with all platform point movements (Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment)
- Redemption Log tab with every completed redemption, NOK value, and welfare tag
- Company Activity tab with per-company breakdown (Bookings Made, Bookings Received, Redemptions, Current Balance) plus activity table
- Employee Activity tab with per-employee usage, total NOK value, welfare benefits total, and count
- Filters on each tab: company, type (for transactions), date range
- Excel (XLSX) export for each of the four log types with professional formatting, color-coded values, and summary totals
- Pagination (20 entries per page)

### Feature 15: Estimated Value Field
- NOK value displayed prominently on experience cards, detail pages, and admin experience list
- NOK value stored with each ticket and usage log at time of booking
- NOK value included in all log tables and Excel exports
- NOK value appears in redemption log for tax documentation

### Feature 16: Welfare Classification
- Welfare badge displayed on experience detail pages and cards (green "Yes" or gray "No")
- Welfare status stored with every ticket and usage log
- Welfare tag visible in admin redemption log, employee activity log, and Tax Reports
- Welfare status available as a filter on the Tax Reports page

### Feature 17: Usage Documentation
- Automatic usage log entry created on every ticket redemption
- Log captures: employee name, experience title, date, NOK value, host company, welfare tag, points cost
- Usage logs stored in a dedicated append-only table for audit integrity
- Tax Reports page (sidebar: "Tax Reports") accessible by Owner and Manager roles
- Filters on Tax Reports: employee, welfare status, date range
- Summary bar with Total NOK Value, Welfare Benefits Total, and Total Redemptions
- Data ready to feed into future yearly employee summary and CSV tax export (M8)

### Additional Deliverables (Beyond M7 Scope)
- Multi-Language Support for M7: complete English/Norwegian translations for Admin Dashboard, Admin Companies, Admin Experiences, Admin Usage Logs (all 4 tabs), and Tax Reports
- VAT Invoice Plan - Design Deliverables: complete design package for the future VAT/Invoicing module (10 HTML/CSS interactive screens, wireframes, user journey map, and platform flow diagram) based on client's scope clarification request

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (5 phases covering F11, F12, F15, F16, F17) | ✅ |
| 2 | Platform Flow Diagram - Admin Dashboard & Tax Module Part 1 | ✅ |
| 3 | Wireframes (11 screens) | ✅ |
| 4 | HTML/CSS Design Templates | ✅ |
| 5 | Backend - Usage logs migration (append-only) | ✅ |
| 6 | Backend - UsageLog model with auto-creation on redemption | ✅ |
| 7 | Backend - Admin Dashboard API (metrics, charts, recent activity) | ✅ |
| 8 | Backend - Admin Companies API (list, detail, activate/suspend) | ✅ |
| 9 | Backend - Admin Experiences API (list, detail, filters) | ✅ |
| 10 | Backend - Usage Logs API (4 types with filters) | ✅ |
| 11 | Backend - Excel Export API (4 types with XLSX formatting) | ✅ |
| 12 | Backend - Tax Reports (Usage Documentation) API | ✅ |
| 13 | Frontend - Admin Dashboard page | ✅ |
| 14 | Frontend - Admin Companies (list + detail) | ✅ |
| 15 | Frontend - Admin Experiences (list + detail with NOK & welfare) | ✅ |
| 16 | Frontend - Admin Usage Logs (4 tabs with filters and exports) | ✅ |
| 17 | Frontend - Tax Reports (Usage Documentation) page | ✅ |
| 18 | Frontend - Sidebar updates (Admin sections + Tax Reports) | ✅ |
| 19 | Multi-Language Support for M7 (Additional) | ✅ |
| 20 | VAT Invoice Plan - Design Package (Additional) | ✅ |
| 21 | Server Deployment | ✅ |
| 22 | Release Notes | ✅ |

---

## Screens Delivered

| # | Screen | Type |
|---|--------|------|
| 1 | Admin Dashboard Overview | Protected (Super Admin) |
| 2 | Admin Companies - List | Protected (Super Admin) |
| 3 | Admin Companies - Detail | Protected (Super Admin) |
| 4 | Admin Experiences - List | Protected (Super Admin) |
| 5 | Admin Experiences - Detail | Protected (Super Admin) |
| 6 | Admin Usage Logs - Transaction Log | Protected (Super Admin) |
| 7 | Admin Usage Logs - Redemption Log | Protected (Super Admin) |
| 8 | Admin Usage Logs - Company Activity | Protected (Super Admin) |
| 9 | Admin Usage Logs - Employee Activity | Protected (Super Admin) |
| 10 | Tax Reports (Usage Documentation) | Protected (Owner/Manager) |
| 11 | Experience Detail with NOK & Welfare badges | Protected (All Roles) |

---

## API Endpoints Delivered

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/admin/dashboard` | Platform metrics, charts, and recent activity |
| GET | `/api/admin/dashboard/companies` | List all companies with search and pagination |
| GET | `/api/admin/dashboard/companies/{id}` | Company detail with info, stats, and employees |
| POST | `/api/admin/dashboard/companies/{id}/status` | Toggle company active/suspended status |
| GET | `/api/admin/dashboard/experiences` | List all experiences with filters |
| GET | `/api/admin/dashboard/experiences/{id}` | Experience detail with company info |
| GET | `/api/admin/dashboard/logs/transactions` | Transaction log with filters |
| GET | `/api/admin/dashboard/logs/redemptions` | Redemption log with filters |
| GET | `/api/admin/dashboard/logs/company-activity` | Per-company activity log |
| GET | `/api/admin/dashboard/logs/employee-activity` | Per-employee activity log with totals |
| GET | `/api/admin/dashboard/export/transactions` | Transaction log XLSX export |
| GET | `/api/admin/dashboard/export/redemptions` | Redemption log XLSX export |
| GET | `/api/admin/dashboard/export/company-activity` | Company activity XLSX export |
| GET | `/api/admin/dashboard/export/employee-activity` | Employee activity XLSX export |
| GET | `/api/usage-docs` | Tax Reports usage documentation for Owner/Manager |
| GET | `/api/dashboard/company` | Company dashboard data (Owner/Manager) |
| GET | `/api/dashboard/employee` | Employee dashboard data |

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| View Admin Dashboard | ❌ | ❌ | ❌ | ✅ |
| Manage Companies (list, detail, activate/suspend) | ❌ | ❌ | ❌ | ✅ |
| Browse All Experiences (Admin) | ❌ | ❌ | ❌ | ✅ |
| View All Usage Logs (4 types) | ❌ | ❌ | ❌ | ✅ |
| Export Usage Logs to Excel | ❌ | ❌ | ❌ | ✅ |
| View NOK Value on Experiences | ✅ | ✅ | ✅ | ✅ |
| View Welfare Tag on Experiences | ✅ | ✅ | ✅ | ✅ |
| Access Tax Reports (Usage Documentation) | ✅ | ✅ | ❌ | ❌ |
| Filter Tax Reports by Employee / Welfare / Date | ✅ | ✅ | ❌ | ❌ |

---

## Usage Documentation Flow

| Event | Action | Logged |
|-------|--------|--------|
| Ticket Redeemed | Usage log entry auto-created | Employee name, experience, date, NOK value, host company, welfare tag, points cost |
| Tax Reports Opened | Company logs loaded with filters | Total NOK Value, Welfare Benefits Total, Total Redemptions |
| Admin Log Exported | XLSX file generated | Filtered data with formatted header, color-coded values, summary totals |

---

## Excel Export Format

| Element | Detail |
|---------|--------|
| Header | SwapJoys branded title, report name, generation date, filter period |
| Column Headers | Dark blue background (#1B2D4F), white bold text |
| Data Rows | Alternating row colors for readability |
| Points Column | Color-coded: green for positive (+), red for negative (-) |
| NOK Value | Blue bold with number formatting (#,##0.00) |
| Welfare Tag | Green "Yes" or gray "No" |
| Summary | Total records, net points, total NOK, welfare count, total points |
| Filename | `SwapJoys_[ReportName]_YYYY-MM-DD.xlsx` |

---

## Known Limitations

| Limitation |
|------------|
| Yearly employee summary is not yet implemented (Milestone 8) |
| NOK 4,000 threshold warning per employee is not yet implemented (Milestone 8) |
| CSV tax export for employee welfare is not yet implemented (Milestone 8) |
| Legal disclaimer on tax reports is not yet displayed (Milestone 8) |
| Subscription module is not yet available (Milestone 8) |
| Automatic suspension logic based on unpaid invoices is not yet available (Milestone 8) |
| VAT / Invoicing module is delivered as design only; development not yet contracted |
| Company Dashboard with charts for Owner/Manager/Employee is deferred per client request |

---

## Compatibility Notes

| Note |
|------|
| All M1-M6 features remain fully compatible |
| Database schema extended with a dedicated `usage_logs` table (append-only, immutable) |
| Existing `points_ledger` and `bookings` tables are unchanged |
| API contracts stable for all previously delivered features |
| Redemption flow unchanged; usage log creation is additive and transactional |
| Norwegian/English language toggle works consistently across all M7 screens |
| Excel exports require the PhpSpreadsheet library, which is included in the backend environment |

---

<div align="center">

**End of Version 1.6.0 Release Notes**

</div>
