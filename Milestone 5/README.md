# SwapJoys Platform - Release Notes

## Version 1.4.0

![Release Date](https://img.shields.io/badge/Release%20Date-March%2017%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.4.0 delivers the Booking & Verification functionality for the SwapJoys platform. This release enables companies to request experiences from other companies, approve or reject incoming requests, generate tickets with backup codes for redemption, and verify redemption through manual code entry. Points are settled automatically through the booking lifecycle, and email notifications keep all parties informed.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables registered companies to:

- Request experiences from other companies with employee assignment and preferred dates
- Review, approve, or reject incoming experience requests
- Generate tickets with unique 6-character backup codes upon approval
- Verify and redeem tickets through manual backup code entry
- Automatically settle points (deduction on approval, credit on redemption)
- Track booking statuses across all views (Pending, Confirmed, Used, Rejected)
- Receive email notifications for all booking lifecycle events
- Log usage documentation for Norwegian tax compliance on each redemption

> This release completes Milestone 5: Booking & QR Verification (Features 6, 7, 13) and builds on M1 (Foundation), M2 (Company Registration), M3 (Employee Onboarding & Roles), and M4 (Experience Creation & Marketplace).

---

## What's New

- Complete booking request workflow with employee assignment
- Incoming requests management with approve/reject actions
- Ticket generation with unique 6-character alphanumeric backup codes
- Manual backup code entry for ticket redemption
- Automatic points settlement (deduct on approve, credit on redeem)
- Four transactional email notifications (new request, approved, rejected, redeemed)
- Booking status tracking with visual badges across all views
- Usage documentation auto-logged on each redemption for tax records
- Norwegian/English language toggle updates for M5 screens

---

## New Features

### Feature 6: Request/Book Experience
- "Request Experience" button on marketplace experience detail page
- Balance check before request submission (Points ≥ Cost)
- Employee selection dropdown for assigning the experience
- Preferred date picker and optional message to host
- Request submission creates booking record with Pending status
- Email notification sent to host company Owner and Manager(s)
- My Bookings page with Outgoing and Incoming tabs
- Booking stats cards (Total, Pending, Confirmed, Used, Rejected)
- Status filter on outgoing bookings list
- Booking detail views differentiated by status

### Feature 6: Approve/Reject Requests (Host Side)
- Incoming Requests tab with pending request cards and stats
- Request detail view showing company, employee, date, and message
- Approve action with confirmation dialog
- Points deducted from requesting company on approval
- Ticket created with unique backup code on approval
- Transaction log entry created (append-only ledger)
- Reject action with mandatory reason input (minimum 10 characters)
- Rejection notification email sent with reason to requesting company
- Approval notification email sent with backup code to requesting company and assigned employee

### Feature 7: QR Code or Unique Code Verification (Partial)
- Unique 6-character alphanumeric backup code generated per ticket
- Ticket View page displaying backup code for assigned employee
- Scanner/Redeem page with manual backup code entry field
- Code validation logic (valid, unused, not expired, correct host)
- Redemption confirmation screen with ticket summary
- Mark ticket as Used on successful redemption
- Points credited to host company on redemption
- Transaction log entry for points credit
- Usage documentation auto-created (Employee, Experience, Date, Value, Company, Welfare tag)
- Redemption success screen showing points credited
- Redemption notification email sent to requesting company and employee

### Feature 13: Experience Status Tracking
- Status field on all booking and ticket records
- Pending status (orange badge) — when request submitted
- Confirmed status (blue badge) — when host approves
- Used status (green badge) — when ticket is redeemed
- Rejected status (red badge) — when host rejects
- Status badges displayed consistently across My Bookings, Incoming Requests, and all detail views

### Additional Deliverables (Beyond M5 Scope)
- Language toggle (Norwegian/English) updates for all M5 screens

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (6 phases) | ✅ |
| 2 | Platform Flow Diagram - Booking & QR Verification | ✅ |
| 3 | Email Notification Specifications (4 emails) | ✅ |
| 4 | Wireframes (10+ screens) | ✅ |
| 5 | HTML/CSS Design Templates | ✅ |
| 6 | Backend API - Booking Request CRUD | ✅ |
| 7 | Backend API - Approve/Reject with Points Settlement | ✅ |
| 8 | Backend API - Ticket Generation with Backup Code | ✅ |
| 9 | Backend API - Manual Code Redemption | ✅ |
| 10 | Backend API - Email Notifications (4 types) | ✅ |
| 11 | Backend API - Usage Documentation Logging | ✅ |
| 12 | Frontend - Request Experience Form | ✅ |
| 13 | Frontend - My Bookings (Outgoing/Incoming) | ✅ |
| 14 | Frontend - Ticket View with Backup Code | ✅ |
| 15 | Frontend - Scanner/Redeem (Manual Entry) | ✅ |
| 16 | Frontend - Status Badges Across Views | ✅ |
| 17 | Language Toggle Updates for M5 (Additional) | ✅ |
| 18 | Server Deployment | ✅ |
| 19 | Release Notes | ✅ |

---

## Screens Delivered

| # | Screen | Type |
|---|--------|------|
| 1 | Request Experience Form | Protected (Owner/Manager) |
| 2 | My Bookings - Outgoing Tab | Protected (All Roles) |
| 3 | My Bookings - Incoming Tab | Protected (Owner/Manager) |
| 4 | Booking Detail (Pending) | Protected (Owner/Manager) |
| 5 | Booking Detail (Confirmed) | Protected (All Roles) |
| 6 | Booking Detail (Used) | Protected (All Roles) |
| 7 | Booking Detail (Rejected) | Protected (Owner/Manager) |
| 8 | Ticket View with Backup Code | Protected (All Roles) |
| 9 | Scanner/Redeem (Manual Entry) | Protected (Owner/Manager) |
| 10 | Redemption Success | Protected (Owner/Manager) |

---

## API Endpoints Delivered

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/bookings` | Submit booking request |
| GET | `/api/bookings/outgoing` | List outgoing bookings |
| GET | `/api/bookings/incoming` | List incoming requests |
| GET | `/api/bookings/{id}` | Get booking detail |
| GET | `/api/bookings/stats` | Get booking stats by status |
| PATCH | `/api/bookings/{id}/approve` | Approve request (deduct points, create ticket) |
| PATCH | `/api/bookings/{id}/reject` | Reject request with reason |
| GET | `/api/tickets/{id}` | Get ticket detail with backup code |
| POST | `/api/tickets/redeem` | Redeem ticket via manual code entry |

---

## Email Notifications Delivered

| # | Email | Trigger | Recipient |
|---|-------|---------|-----------|
| 1 | New Request Received | Request submitted | Host company Owner + Manager(s) |
| 2 | Request Approved | Host approves | Requesting company Owner + Manager(s) + Employee |
| 3 | Request Rejected | Host rejects | Requesting company Owner + Manager(s) |
| 4 | Ticket Redeemed | Code verified | Requesting company Owner + Manager(s) + Employee |

---

## Points Settlement Flow

| Event | Points Action | Logged |
|-------|---------------|--------|
| Request Submitted | Points checked, NOT deducted | Booking created |
| Host Approves | Points DEDUCTED from requesting company | Transaction log entry |
| Ticket Redeemed | Points CREDITED to host company | Transaction log + Usage documentation |

---

## Role-Based Access

| Action | Owner | Manager | Employee |
|--------|:-----:|:-------:|:--------:|
| Request Experience | ✅ | ✅ | ❌ |
| View Outgoing Bookings | ✅ | ✅ | ✅ |
| View Incoming Requests | ✅ | ✅ | ❌ |
| Approve/Reject Requests | ✅ | ✅ | ❌ |
| View Ticket (Assigned) | ✅ | ✅ | ✅ |
| Scan/Redeem Ticket | ✅ | ✅ | ❌ |
| View Booking Stats | ✅ | ✅ | ❌ |

---

## Status Tracking

| Status | Badge Color | Description |
|--------|-------------|-------------|
| Pending | 🟡 Orange | Request submitted, awaiting host decision |
| Confirmed | 🔵 Blue | Approved, ticket created, points deducted |
| Used | 🟢 Green | Redeemed via backup code, points credited to host |
| Rejected | 🔴 Red | Declined by host with reason |

---

## Known Limitations

| Limitation |
|------------|
| QR code generation is not yet implemented — tickets use 6-character alphanumeric backup codes only |
| QR code display on ticket view is not yet available — backup code is shown as text |
| Full-screen "Show to Host" QR mode is not yet implemented |
| Camera-based QR scanning is not yet available — redemption is via manual backup code entry only |
| Points system dashboard not yet implemented (Milestone 6) |
| Admin dashboard and usage logs not yet available (Milestone 7) |
| Tax documentation module (yearly summary, threshold warnings, CSV export) not yet implemented (Milestones 7-8) |
| Subscription system not yet available (Milestone 8) |

---

## Compatibility Notes

| Note |
|------|
| All M1, M2, M3, and M4 features remain fully compatible |
| Database schema updated with bookings, tickets, and transaction log tables |
| API contracts stable for all delivered features |
| Usage documentation records are created on redemption and ready for Tax Documentation module (Milestone 7) |
| Points ledger uses append-only immutable logging as specified in architecture |

---

<div align="center">

**End of Version 1.4.0 Release Notes**

</div>
