# SwapJoys Platform MVP

![SwapJoys](https://img.shields.io/badge/SwapJoys-Platform-6366f1)
![Version](https://img.shields.io/badge/version-1.2.0--M3-blue)
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
├── Milestone 4/                    # Experience Marketplace (Next)
├── Milestone 5/                    # Booking & QR (Coming)
├── Milestone 6/                    # Points System (Coming)
├── Milestone 7/                    # Admin & Tax Part 1 (Coming)
├── Milestone 8/                    # Tax Part 2 & Launch (Coming)
└── README.md
```

---

## Milestones

| Milestone | Weeks | Duration | Features | Status |
|-----------|-------|----------|----------|--------|
| **M1** | 1-2 | 2 weeks | Foundation Setup | ✅ Complete |
| **M2** | 3-4 | 2 weeks | Company Registration | ✅ Complete |
| **M3** | 5-6 | 2 weeks | Employee Onboarding, Roles | ✅ Complete |
| **M4** | 7-8 | 2 weeks | Experience Creation, Marketplace | 🔄 Next |
| **M5** | 9-10 | 2 weeks | Booking, QR Verification, Status | ⏳ Planned |
| **M6** | 11-12 | 2 weeks | Points System, Balance, Override | ⏳ Planned |
| **M7** | 13-14 | 2 weeks | Admin Dashboard, Tax Part 1 | ⏳ Planned |
| **M8** | 15-16 | 2 weeks | Tax Part 2, Subscription, Launch | ⏳ Planned |
| **M9** | TBD | TBD | Stripe Integration + Final QA | ⏳ Planned |

**Total Timeline:** 16+ weeks | 8+ Milestones | 21 Features

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
