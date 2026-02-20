# SwapJoys Platform - Release Notes

## Version 1.2.0

![Release Date](https://img.shields.io/badge/Release%20Date-February%2020%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.2.0 delivers Employee Onboarding and Role Assignment functionality for the SwapJoys platform. This release enables companies to add employees, manage roles with a three-tier permission system, and control access across the platform.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables registered companies to:

- Create and publish employee experiences
- Add and manage employees with email invitations
- Assign roles (Owner / Manager / Employee) with granular permissions
- Control access to features based on assigned roles

> This release builds on M1 (Foundation) and M2 (Company Registration) to complete Module 1: Company & Employee Onboarding.

---

## What's New

- Complete employee onboarding with email invitation system
- Three-tier role-based access control (Owner / Manager / Employee)
- Employee list with search, filter, and pagination
- Account activation flow for invited employees
- New landing page design with modern layout
- Full project color scheme update
- Norwegian/English language toggle across full website
- Profile management in Settings

---

## New Features

### Feature 2: Employee Onboarding
- Employee list page with stats cards (Total, Active, Pending, Managers)
- Add Employee modal with form validation
- Email invitation system with 7-day token expiry
- Account activation page for invited employees
- Activation success screen with countdown redirect
- Resend invitation functionality
- Employee search by name or email
- Filter by role and status
- Pagination for large employee lists
- Employee detail view and edit functionality
- Deactivate/Activate employee toggle
- Empty state design for companies with no employees

### Feature 3: Role Assignment
- Three-tier role system: Owner / Manager / Employee
- Role-based permission matrix implementation
- Owner: Full access including billing, settings, role management
- Manager: Manage employees, experiences, approve bookings, view reports
- Employee: View marketplace, use tickets, view own bookings
- Role change dropdown (Owner only)
- Last Owner protection (cannot demote the only Owner)
- Role-based sidebar navigation (different menus per role)
- Laravel middleware for backend route protection
- React route guards for frontend route protection
- Role badges displayed on employee list

### Additional Deliverables (Beyond M3 Scope)
- New landing page with complete redesign and modern layout
- 9 AI-generated images created and integrated into landing page
- Full project color scheme change based on new landing page design
- Language toggle (Norwegian/English) across full website
- Profile section added in Settings page

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (5 phases) | ✅ |
| 2 | Platform Flow Diagram - Employee Onboarding | ✅ |
| 3 | Wireframes (8 screens) | ✅ |
| 4 | HTML/CSS Design Templates | ✅ |
| 5 | Backend API - Employee Onboarding | ✅ |
| 6 | Backend API - Role Assignment & Permissions | ✅ |
| 7 | Frontend - Employee Management Pages | ✅ |
| 8 | Frontend - Account Activation Flow | ✅ |
| 9 | Frontend - Role-Based Navigation | ✅ |
| 10 | New Landing Page Design (Additional) | ✅ |
| 11 | 9 AI-Generated Images (Additional) | ✅ |
| 12 | Full Color Scheme Change (Additional) | ✅ |
| 13 | Language Toggle NO/EN (Additional) | ✅ |
| 14 | Profile in Settings (Additional) | ✅ |
| 15 | Server Deployment | ✅ |
| 16 | Release Notes | ✅ |

---

## Known Limitations

| Limitation |
|------------|
| Employee bulk import is not included (single add only) |
| Role permissions are predefined and not customizable |
| Invitation email template is basic and may be refined in future milestones |

---

## Compatibility Notes

| Note |
|------|
| API contracts are stable for M1-M3 features |
| Database schema updated with employee and role tables |
| Role-based navigation requires login refresh to reflect role changes |

---

<div align="center">

**End of Version 1.2.0 Release Notes**

</div>
