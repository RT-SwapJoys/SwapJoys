# SwapJoys Platform - Release Notes

## Version 1.1.0

![Release Date](https://img.shields.io/badge/Release%20Date-January%2030%2C%202026-blue)
![Status](https://img.shields.io/badge/Status-Stable-success)
![Prepared by](https://img.shields.io/badge/Prepared%20by-Rebing%20Tech-purple)

---

## Overview

Version 1.1.0 delivers the complete Company Registration feature (Feature 1) for the SwapJoys platform. This release enables companies to register, verify their email, log in, manage their profile, and access the platform dashboard.

SwapJoys is a B2B Employee Experience Exchange Platform that enables companies to exchange employee benefits through a points-based marketplace.

---

## Platform Summary

The platform now enables companies to:

- Register with email verification and receive 50 welcome points
- Log in securely with JWT authentication
- Reset forgotten passwords via email
- View and manage company profile information

> This release completes Milestone 2: Company Registration (Feature 1) with production deployment.

---

## What's New

- Landing page with animated hero section and responsive design
- Complete company registration flow with validation
- Email verification system with 24-hour token expiry
- Secure login with JWT token management
- Password reset functionality with 1-hour token expiry
- Company profile management
- Production deployment on swapjoys.com

---

## New Features

### Landing Page
- Modern animated hero section with floating cards
- Responsive design for all screen sizes (mobile, tablet, desktop)
- Feature highlights (Welcome Points, QR Verification, Tax Reports)
- Login and Register navigation buttons
- SwapJoys branding and footer

### Company Registration (Feature 1)
- Registration form with comprehensive validation
- Email address with format and uniqueness validation
- Password with strength requirements (8+ chars, uppercase, number)
- Company name and organization number (Norwegian 9-digit format)
- Address and city selection from dropdown
- Terms & Conditions acceptance checkbox
- Automatic +50 welcome points credited on successful registration

### Email Verification
- Verification email sent immediately after registration
- Secure token with 24-hour expiry
- "Check Your Email" screen with step-by-step instructions
- Resend verification email functionality
- Email verified success screen with welcome bonus display
- Automatic redirect to login after verification

### Login System
- Secure login form with email and password
- JWT token generation and secure storage
- "Remember me" functionality
- Email verification check before allowing login
- Role detection for dashboard redirect (Owner/Manager/Employee)
- Session management with logout functionality

### Password Reset
- "Forgot Password" link on login page
- Password reset request form
- Reset email with secure 1-hour token
- New password form with strength validation
- Password requirements display with real-time feedback
- Automatic redirect to login after successful reset

### Company Profile
- Profile page with company information display
- Edit functionality for all company fields
- Company avatar with initials
- Verified email badge display
- Points balance display
- Save and cancel actions

### Additional Features (Beyond Original Scope)
- Terms & Conditions page
- Privacy Policy page
- Settings page with change password functionality
- Dashboard layout with sidebar navigation
- Protected routes for unverified users
- Language toggle (Norwegian/English)

---

## Deliverables

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | User Journey Map (4 phases documented) | ✅ |
| 2 | HTML/CSS Design Templates (7 screens) | ✅ |
| 3 | Landing Page (responsive, animated) | ✅ |
| 4 | Registration API with validation | ✅ |
| 5 | Email verification system (24hr token) | ✅ |
| 6 | Login API with JWT authentication | ✅ |
| 7 | Password reset system (1hr token) | ✅ |
| 8 | Company profile API (GET/PUT) | ✅ |
| 9 | React frontend (all screens) | ✅ |
| 10 | Production deployment (swapjoys.com) | ✅ |
| 11 | Domain, hosting, and email setup | ✅ |
| 12 | Terms & Conditions page (Additional) | ✅ |
| 13 | Privacy Policy page (Additional) | ✅ |
| 14 | Settings with change password (Additional) | ✅ |
| 15 | Language toggle NO/EN (Additional) | ✅ |

---

## Screens Delivered

| # | Screen | Type |
|---|--------|------|
| 1 | Landing Page | Public |
| 2 | Registration | Public |
| 3 | Verification Pending | Public |
| 4 | Email Verified | Public |
| 5 | Login | Public |
| 6 | Forgot Password | Public |
| 7 | Reset Password | Public |
| 8 | Dashboard | Protected |
| 9 | Company Profile | Protected |
| 10 | Settings | Protected |
| 11 | Terms & Conditions | Public |
| 12 | Privacy Policy | Public |

---

## API Endpoints Delivered

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/register` | Company registration |
| POST | `/api/login` | User login |
| POST | `/api/logout` | User logout |
| GET | `/api/verify-email/{token}` | Email verification |
| POST | `/api/resend-verification` | Resend verification email |
| POST | `/api/password/forgot` | Request password reset |
| POST | `/api/password/reset` | Reset password |
| GET | `/api/company` | Get company profile |
| PUT | `/api/company` | Update company profile |
| POST | `/api/password/change` | Change password (authenticated) |

---

## Infrastructure Setup

| Service | Details |
|---------|---------|
| Domain | swapjoys.com (.COM) |
| Hosting | KVM 2 VPS |
| SSL Certificate | Let's Encrypt (HTTPS enabled) |
| Email Service | Business email configured |

---

## Known Limitations

| Limitation |
|------------|
| Employee onboarding not yet implemented (Milestone 3) |
| Experience marketplace not yet available (Milestone 4) |
| Points can only be earned through welcome bonus currently |
| Admin dashboard not yet available (Milestone 7) |
| Subscription/payment not yet implemented (Milestone 8) |

---

## Compatibility Notes

| Note |
|------|
| All Milestone 1 foundation components remain compatible |
| Database schema unchanged from Milestone 1 |
| API versioning not yet implemented |
| Mobile app not included in MVP scope |

<div align="center">

**End of Version 1.1.0 Release Notes**

</div>
