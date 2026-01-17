# SwapJoys Platform Flow Diagram

> Complete user journey map covering all 21 MVP features

---

## 📊 View Diagram

**🔗 Interactive Diagram:** [Open in Mermaid](https://mermaid.ai/d/8fd9a817-569a-4841-b7e7-45a07413a7ca)

---

## Diagram Coverage

This flow diagram maps the complete user journey for the SwapJoys Platform MVP:

### Platform Entry
| Flow | Description |
|------|-------------|
| Landing Page | Entry point for new and existing users |
| Login | Authentication for existing users |
| Role Detection | Routes users to appropriate dashboard |

### User Dashboards
| Role | Access Level |
|------|--------------|
| Owner | Full access: billing, settings, all features |
| Manager | Manage employees, experiences, view reports |
| Employee | View experiences, redeem tickets |
| SwapJoys Admin | Platform administration |

### Feature Flows Covered

| Module | Features | Flow IDs |
|--------|----------|----------|
| Company & Employee Onboarding | Company Registration, Employee Onboarding, Role Assignment | F1, F2, F3 |
| Experience Marketplace | Create Experience, Browse Experiences, Request/Book, QR Verification | F4, F5, F6, F7 |
| Points & Balance | Fixed-Point System, Company Balance, Admin Override | F8, F9, F10 |
| Admin Tools | Admin Dashboard, Usage Logs, Status Tracking | F11, F12, F13 |
| Subscription | Company Membership Payment | F14 |
| Tax Documentation | Value Field, Welfare Tag, Usage Docs, Summary, Threshold, Export, Disclaimer | F15-F21 |

---

## Key User Journeys

### 1. Company Registration Flow (F1)
```
Enter Email & Password → Company Details → Accept Terms → Submit → 
Email Verification → Verify Link → +50 Welcome Points → Complete Profile → Login
```

### 2. Experience Booking Flow (F5-F7)
```
Browse Marketplace → Filter (Category/City) → View Details → Request Experience → 
Check Balance → Select Employee → Choose Date → Submit Request → 
Host Approval → Points Deducted → QR Ticket Generated → Redeem → Points Credited
```

### 3. Tax Documentation Flow (F15-F21)
```
Experience Redeemed → Auto-Log Usage → Track Value (NOK) → Welfare Tag → 
Yearly Summary Calculated → Threshold Warning (NOK 5,000) → CSV Export Available
```

---

## Technical Notes

- **Format:** Mermaid Flowchart
- **Created:** January 2026
- **Milestone:** 1 (Foundation Setup)
- **Status:** ✅ Approved by Client

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 1 of 8
