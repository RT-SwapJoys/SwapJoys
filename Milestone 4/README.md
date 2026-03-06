# SwapJoys Platform - Release Notes

## Version 1.3.0

![Release Date](https://img.shields.io/badge/Release%20Date-March%206%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.3.0 delivers the Experience Creation and Marketplace functionality for the SwapJoys platform. This release enables companies to create, publish, and manage experiences, and allows all users to browse, search, and filter available experiences from other companies on the marketplace.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables registered companies to:

- Create and publish employee experiences with photos, categories, and pricing
- Manage company experiences (edit, deactivate, reactivate)
- Browse a marketplace of experiences offered by other companies
- Search and filter experiences by category and city
- View detailed experience information including tax-related fields
- Track estimated values and welfare classifications for Norwegian tax compliance

> This release completes Milestone 4: Experience Creation & Marketplace (Features 4, 5) and builds on M1 (Foundation), M2 (Company Registration), and M3 (Employee Onboarding & Roles).

---

## What's New

- Complete experience creation flow with photo upload
- My Experiences management page with stats overview
- Experience marketplace with card grid layout
- Category and city filters with combined filtering
- Search by experience title or company name
- Experience detail page with host company information
- Tax documentation fields (Estimated Value, Welfare Classification)
- Norwegian/English language toggle updates for M4 screens

---

## New Features

### Feature 4: Create Experience
- Create Experience form with comprehensive field validation
- Title, description, capacity, rules/terms input fields
- Photo upload with preview (JPG/PNG, max 5MB)
- Point cost setting for experience exchange
- Estimated Value (NOK) field for tax documentation
- Welfare Classification mandatory tag (Yes/No)
- Category selection (Dining, Wellness, Entertainment, Activities, Culture, Travel, Other)
- City selection from Norwegian cities dropdown
- Publish experience to make visible on marketplace
- My Experiences page with grid layout
- Experience stats cards (Total, Active, Inactive)
- Edit Experience form with pre-loaded data and photo replacement
- Deactivate/Activate experience toggle with confirmation modal
- Empty state design for companies with no experiences

### Feature 5: Browse Experiences (Marketplace)
- Marketplace page displaying active experiences from other companies
- Experience card grid layout showing photo, title, company, points, city, and category
- Category filter dropdown
- City filter dropdown
- Combined filter logic (category + city work together)
- Search functionality by experience title or company name
- Experience Detail page with full information display
- Large photo display with experience details
- Host company information section
- Tax fields display (Estimated Value badge, Welfare Classification badge)
- "Request Experience" button (placeholder for Milestone 5)
- Back to Marketplace navigation
- Company's own experiences excluded from marketplace view

### Additional Deliverables (Beyond M4 Scope)
- Language toggle (Norwegian/English) updates for all M4 screens

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (4 phases) | ✅ |
| 2 | Platform Flow Diagram - Experience Creation & Marketplace | ✅ |
| 3 | Wireframes (7 screens) | ✅ |
| 4 | HTML/CSS Design Templates | ✅ |
| 5 | Backend API - Experience CRUD | ✅ |
| 6 | Backend API - Marketplace Browse, Search & Filter | ✅ |
| 7 | Backend API - Photo Upload & Storage | ✅ |
| 8 | Frontend - Create Experience Page | ✅ |
| 9 | Frontend - My Experiences Management | ✅ |
| 10 | Frontend - Marketplace Browse Page | ✅ |
| 11 | Frontend - Experience Detail Page | ✅ |
| 12 | Language Toggle Updates for M4 (Additional) | ✅ |
| 13 | Server Deployment | ✅ |
| 14 | Release Notes | ✅ |

---

## Screens Delivered

| # | Screen | Type |
|---|--------|------|
| 1 | Create Experience | Protected (Owner/Manager) |
| 2 | My Experiences | Protected (Owner/Manager) |
| 3 | Edit Experience | Protected (Owner/Manager) |
| 4 | Marketplace | Protected (All Roles) |
| 5 | Experience Detail | Protected (All Roles) |
| 6 | Experience Detail (Owner View) | Protected (Owner/Manager) |
| 7 | Empty State (No Experiences) | Protected (Owner/Manager) |

---

## API Endpoints Delivered

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/experiences` | Create new experience |
| GET | `/api/experiences` | List company's own experiences |
| GET | `/api/experiences/{id}` | Get experience detail |
| PUT | `/api/experiences/{id}` | Update experience |
| PATCH | `/api/experiences/{id}/deactivate` | Deactivate experience |
| PATCH | `/api/experiences/{id}/activate` | Activate experience |
| POST | `/api/experiences/{id}/photo` | Upload experience photo |
| GET | `/api/marketplace` | Browse marketplace experiences |
| GET | `/api/marketplace/{id}` | Get marketplace experience detail |
| GET | `/api/categories` | List experience categories |
| GET | `/api/cities` | List available cities |

---

## Role-Based Access

| Action | Owner | Manager | Employee |
|--------|:-----:|:-------:|:--------:|
| Create Experience | ✅ | ✅ | ❌ |
| Edit Experience | ✅ | ✅ | ❌ |
| Deactivate/Activate | ✅ | ✅ | ❌ |
| View My Experiences | ✅ | ✅ | ❌ |
| Browse Marketplace | ✅ | ✅ | ✅ |
| View Experience Detail | ✅ | ✅ | ✅ |

---

## Known Limitations

| Limitation |
|------------|
| Single photo per experience (gallery not supported) |
| Booking/request workflow not yet implemented (Milestone 5) |
| QR code verification not yet available (Milestone 5) |
| Points transfer on redemption not yet implemented (Milestone 6) |
| Experience search is basic text match (no fuzzy search) |

---

## Compatibility Notes

| Note |
|------|
| All M1, M2, and M3 features remain fully compatible |
| Database schema updated with experiences, categories, and cities tables |
| API contracts stable for all delivered features |
| Estimated Value and Welfare Classification fields are stored and ready for Tax Documentation module (Milestone 7) |

---

<div align="center">

**End of Version 1.3.0 Release Notes**

</div>
