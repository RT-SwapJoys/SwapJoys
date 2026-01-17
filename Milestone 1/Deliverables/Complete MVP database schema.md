# Complete MVP Database Schema

> Database architecture for SwapJoys Platform MVP covering all 21 features

---

## 📊 ERD Diagram

**🔗 Interactive ERD:** [Open in Mermaid](https://mermaid.ai/d/9cc4cc2b-fc49-44b2-8bb6-705f1b9aa670)

---

## Overview

| | |
|---|---|
| **Database** | MySQL |
| **Total Tables** | 18 |
| **Status** | ✅ Complete (MVP Scope) |
| **Version** | 1.0 |
| **Created** | January 2026 |

---

## Tables by Module

| Module | Tables |
|--------|--------|
| Company & Employee Onboarding | companies, users, roles |
| Experience Marketplace | experiences, categories, cities, bookings, tickets |
| Points & Balance | points_ledger, transactions |
| Admin Tools | admin_users, admin_logs, point_adjustments |
| Tax Documentation | usage_logs, employee_yearly_summaries |
| Subscription | subscriptions, invoices |
| Authentication | password_resets, email_verifications |

---

## Key Relationships

- `companies` → has many → `users`, `experiences`, `bookings`
- `users` → belongs to → `roles` (Owner / Manager / Employee)
- `experiences` → belongs to → `categories`, `cities`
- `bookings` → generates → `tickets`
- `tickets` → logs to → `usage_logs` (Tax Documentation)
- `subscriptions` → has many → `invoices`

---

## Architecture Principles

| Principle | Implementation |
|-----------|----------------|
| Immutable Ledger | `points_ledger`, `transactions` are append-only |
| Tax Compliance | `usage_logs`, `employee_yearly_summaries` for Norwegian tax |
| RBAC | 3-tier role system (Owner, Manager, Employee) |
| GDPR | Data minimization, retention rules |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 1 of 8
