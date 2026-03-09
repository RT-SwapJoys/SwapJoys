# SwapJoys Platform - Wireframes
## Milestone 5: Booking & QR Verification (Features 6, 7, 13)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 5 of 8 |
| **Features** | Request/Book Experience (F6), QR/Unique Code Verification (F7), Experience Status Tracking (F13) |
| **Prepared by** | Rebing Tech |
| **Date** | March 2026 |
| **Status** | Ready for Client Approval |

---

## Screen List

| # | Screen | Type | Actor |
|---|--------|------|-------|
| 1 | Request Experience Modal | Modal over Experience Detail | Owner/Manager |
| 2 | My Bookings — Outgoing Tab | Full Page | Owner/Manager/Employee |
| 3 | My Bookings — Incoming Requests Tab | Full Page | Host Owner/Manager |
| 4 | Request Detail Modal (Incoming) | Modal | Host Owner/Manager |
| 5 | Rejection Reason Modal | Modal | Host Owner/Manager |
| 6 | Booking Detail Modal (Outgoing) | Modal | Owner/Manager/Employee |
| 7 | Ticket View Page | Full Page | Assigned Employee |
| 8 | QR Full-Screen Mode | Full Screen Overlay | Assigned Employee |
| 9 | Scanner Page | Full Page | Host Owner/Manager |
| 10 | Manual Code Entry | Inline on Scanner | Host Owner/Manager |
| 11 | Redemption Success Screen | Full Page / Modal | Host Owner/Manager |
| 12 | Insufficient Points Warning | Inline on Request Modal | Owner/Manager |

---

## Screen 1: Request Experience Modal

```
┌─────────────────────────────────────────────────┐
│  ✕ Close                                        │
│                                                 │
│  📩  Request Experience                         │
│  ─────────────────────────────────────────────  │
│                                                 │
│  Experience: "Spa Day Package"                  │
│  Host: Nordic Wellness AS                       │
│  Cost: 50 points                                │
│  Your Balance: 1,250 points  ✅ Sufficient      │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│  Select Employee *                              │
│  ┌─────────────────────────────────────────┐    │
│  │ ▼  Choose employee                      │    │
│  └─────────────────────────────────────────┘    │
│  Employees: Kari N., Ole S., Per H., ...        │
│                                                 │
│  Preferred Date *                               │
│  ┌─────────────────────────────────────────┐    │
│  │ 📅  Select date                         │    │
│  └─────────────────────────────────────────┘    │
│                                                 │
│  Message to Host (optional)                     │
│  ┌─────────────────────────────────────────┐    │
│  │                                         │    │
│  │  e.g. "We'd love to attend on a Friday" │    │
│  │                                         │    │
│  └─────────────────────────────────────────┘    │
│  Max 500 characters                             │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│         [ Cancel ]    [ Submit Request ▸ ]       │
│                                                 │
└─────────────────────────────────────────────────┘
```

**Insufficient Points Variant:**
```
│  Cost: 80 points                                │
│  Your Balance: 50 points  ⚠️ Insufficient       │
│                                                 │
│  ┌─────────────────────────────────────────┐    │
│  │  ⚠️  Your company needs 30 more points  │    │
│  │     to request this experience.          │    │
│  └─────────────────────────────────────────┘    │
│                                                 │
│  (Form fields disabled, submit button grayed)   │
```

---

## Screen 2: My Bookings — Outgoing Tab

```
┌──────────────────────────────────────────────────────────┐
│  [Sidebar]  │  My Bookings                               │
│             │  Track your experience requests and tickets │
│  Dashboard  │                                            │
│  Marketplace│  ┌──────────────┐ ┌──────────────┐ ┌─────  │
│  My Bookings│  │ 📊 Total: 12 │ │ ⏳ Pending: 3│ │ ✅ Co │
│  ▸ active   │  └──────────────┘ └──────────────┘ └─────  │
│  Points     │  ┌──────────────┐ ┌──────────────┐         │
│  Employees  │  │ ✔️ Used: 5   │ │ ❌ Rejected:1│         │
│  Experiences│  └──────────────┘ └──────────────┘         │
│  Tax Reports│                                            │
│  Settings   │  [ Outgoing ▾ active ]  [ Incoming ]       │
│             │                                            │
│             │  Filter: [ All Statuses ▼ ]  🔍 Search     │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🟡 PENDING                          │   │
│             │  │  Spa Day Package                     │   │
│             │  │  Host: Nordic Wellness AS            │   │
│             │  │  Employee: Kari Nordmann             │   │
│             │  │  Date: Mar 15, 2026  |  50 pts      │   │
│             │  │  Requested: Mar 9, 2026             │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🔵 CONFIRMED                        │   │
│             │  │  Team Dinner at Fjord Restaurant     │   │
│             │  │  Host: Bergen Dining Co              │   │
│             │  │  Employee: Ole Svendsen              │   │
│             │  │  Date: Mar 10, 2026  |  30 pts      │   │
│             │  │  [ View Ticket 🎫 ]                  │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🟢 USED                             │   │
│             │  │  Rock Climbing Session               │   │
│             │  │  Host: Active Life AS                │   │
│             │  │  Employee: Per Hansen                │   │
│             │  │  Redeemed: Mar 5, 2026  |  35 pts   │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🔴 REJECTED                         │   │
│             │  │  Wine Tasting Evening                │   │
│             │  │  Host: Vinbar Oslo AS                │   │
│             │  │  Reason: "Fully booked for March"    │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  [ ◀ ] [ 1 ] [ 2 ] [ ▶ ]                  │
└──────────────────────────────────────────────────────────┘
```

---

## Screen 3: My Bookings — Incoming Requests Tab

```
┌──────────────────────────────────────────────────────────┐
│  [Sidebar]  │  My Bookings                               │
│             │  Manage incoming and outgoing requests      │
│             │                                            │
│             │  ┌──────────────┐ ┌──────────────┐ ┌─────  │
│             │  │ 📥 Total: 8  │ │ ⏳ Pending: 2│ │ ✅ Ap │
│             │  └──────────────┘ └──────────────┘ └─────  │
│             │                                            │
│             │  [ Outgoing ]  [ Incoming ▾ active ]       │
│             │                                            │
│             │  Filter: [ All Statuses ▼ ]  🔍 Search     │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🟡 PENDING            Mar 8, 2026  │   │
│             │  │  "Team Dinner at Fjord Restaurant"   │   │
│             │  │  From: TechCorp AS                   │   │
│             │  │  Employee: Maria Olsen               │   │
│             │  │  Preferred Date: Mar 20, 2026        │   │
│             │  │  Points: 30                          │   │
│             │  │                                      │   │
│             │  │  [ ✅ Approve ]  [ ❌ Reject ]        │   │
│             │  │  [ 👁️ View Details ]                  │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🟡 PENDING            Mar 7, 2026  │   │
│             │  │  "Spa Day Package"                   │   │
│             │  │  From: Startup Hub AS                │   │
│             │  │  Employee: Erik Johansen             │   │
│             │  │  Preferred Date: Mar 22, 2026        │   │
│             │  │  Points: 50                          │   │
│             │  │                                      │   │
│             │  │  [ ✅ Approve ]  [ ❌ Reject ]        │   │
│             │  │  [ 👁️ View Details ]                  │   │
│             │  └─────────────────────────────────────┘   │
│             │                                            │
│             │  ┌─────────────────────────────────────┐   │
│             │  │  🔵 CONFIRMED          Mar 3, 2026  │   │
│             │  │  "Team Dinner at Fjord Restaurant"   │   │
│             │  │  From: DesignLab AS                  │   │
│             │  │  Employee: Anna Berg                 │   │
│             │  │  [ 📷 Scan Ticket ]                  │   │
│             │  └─────────────────────────────────────┘   │
└──────────────────────────────────────────────────────────┘
```

---

## Screen 4: Request Detail Modal (Incoming — Host View)

```
┌─────────────────────────────────────────────────┐
│  📩  Incoming Request            ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  Status: 🟡 Pending                             │
│                                                 │
│  EXPERIENCE                                     │
│  Team Dinner at Fjord Restaurant                │
│  🍽️ Dining  ·  📍 Oslo  ·  30 points           │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│  REQUESTING COMPANY                             │
│  ┌─────────────────────────────────────────┐    │
│  │  [TC]  TechCorp AS                      │    │
│  │        Oslo, Norway                     │    │
│  │        Balance: 450 points              │    │
│  └─────────────────────────────────────────┘    │
│                                                 │
│  ASSIGNED EMPLOYEE                              │
│  Maria Olsen  ·  maria@techcorp.no              │
│                                                 │
│  PREFERRED DATE                                 │
│  📅 March 20, 2026                              │
│                                                 │
│  MESSAGE                                        │
│  "We'd love to book this for our team lead      │
│   as a reward for Q1 performance."              │
│                                                 │
│  SUBMITTED                                      │
│  March 8, 2026 at 14:32                         │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│    [ ❌ Reject ]              [ ✅ Approve ▸ ]   │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

## Screen 5: Rejection Reason Modal

```
┌─────────────────────────────────────────────────┐
│  ❌  Reject Request              ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  You're rejecting the request from TechCorp AS  │
│  for "Team Dinner at Fjord Restaurant".         │
│                                                 │
│  Reason for rejection *                         │
│  ┌─────────────────────────────────────────┐    │
│  │                                         │    │
│  │  e.g. "Fully booked for March. Please   │    │
│  │  try again for April availability."     │    │
│  │                                         │    │
│  └─────────────────────────────────────────┘    │
│  Min 10 characters · Max 500 characters         │
│                                                 │
│  ⚠️  The requesting company will be notified    │
│     with your reason.                           │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│       [ Cancel ]    [ Confirm Rejection ▸ ]     │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

## Screen 6: Booking Detail Modal (Outgoing — Requester View)

```
┌─────────────────────────────────────────────────┐
│  📋  Booking Detail              ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  Status: 🔵 Confirmed                           │
│                                                 │
│  EXPERIENCE                                     │
│  ┌─────────────────────────────────────────┐    │
│  │  [ Experience Photo ]                   │    │
│  └─────────────────────────────────────────┘    │
│  Team Dinner at Fjord Restaurant                │
│  🍽️ Dining  ·  📍 Oslo  ·  30 points           │
│                                                 │
│  HOST COMPANY                                   │
│  [BDC]  Bergen Dining Co  ·  Oslo               │
│                                                 │
│  ASSIGNED EMPLOYEE                              │
│  Ole Svendsen  ·  ole@yourcompany.no            │
│                                                 │
│  PREFERRED DATE                                 │
│  📅 March 10, 2026                              │
│                                                 │
│  POINTS DEDUCTED                                │
│  −30 points on March 5, 2026                    │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│            [ 🎫 View Ticket & QR ]              │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

## Screen 7: Ticket View Page

```
┌──────────────────────────────────────────────────────────┐
│  ← Back to My Bookings                                   │
│                                                          │
│  ┌──────────────────────────────────────────────────┐    │
│  │                                                  │    │
│  │            🎫  YOUR TICKET                       │    │
│  │                                                  │    │
│  │  Status: 🔵 Confirmed                            │    │
│  │                                                  │    │
│  │  ──────────────────────────────────────────────  │    │
│  │                                                  │    │
│  │  EXPERIENCE                                      │    │
│  │  Team Dinner at Fjord Restaurant                 │    │
│  │  🍽️ Dining  ·  📍 Oslo                           │    │
│  │                                                  │    │
│  │  HOST                                            │    │
│  │  Bergen Dining Co                                │    │
│  │                                                  │    │
│  │  EMPLOYEE                                        │    │
│  │  Ole Svendsen                                    │    │
│  │                                                  │    │
│  │  DATE                                            │    │
│  │  📅 March 10, 2026                               │    │
│  │                                                  │    │
│  │  POINTS                                          │    │
│  │  30 points                                       │    │
│  │                                                  │    │
│  │  ──────────────────────────────────────────────  │    │
│  │                                                  │    │
│  │          ┌──────────────────────┐                │    │
│  │          │                      │                │    │
│  │          │    ██ ▄▄ ██ ▄▄ ██   │                │    │
│  │          │    ▄▄ ██ ▄▄ ██ ▄▄   │                │    │
│  │          │    ██ ▄▄ ██ ▄▄ ██   │                │    │
│  │          │    ▄▄ ██ ▄▄ ██ ▄▄   │                │    │
│  │          │    ██ ▄▄ ██ ▄▄ ██   │                │    │
│  │          │                      │                │    │
│  │          └──────────────────────┘                │    │
│  │              [ QR CODE ]                         │    │
│  │                                                  │    │
│  │          Backup Code: A7K9M2                     │    │
│  │                                                  │    │
│  │  ──────────────────────────────────────────────  │    │
│  │                                                  │    │
│  │       [ 📱 Show to Host — Full Screen ]          │    │
│  │                                                  │    │
│  └──────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────┘
```

---

## Screen 8: QR Full-Screen Mode

```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│                    (Dark Background)                     │
│                                                          │
│                                                          │
│                                                          │
│              ┌────────────────────────────┐              │
│              │                            │              │
│              │      ██ ▄▄ ██ ▄▄ ██       │              │
│              │      ▄▄ ██ ▄▄ ██ ▄▄       │              │
│              │      ██ ▄▄ ██ ▄▄ ██       │              │
│              │      ▄▄ ██ ▄▄ ██ ▄▄       │              │
│              │      ██ ▄▄ ██ ▄▄ ██       │              │
│              │      ▄▄ ██ ▄▄ ██ ▄▄       │              │
│              │      ██ ▄▄ ██ ▄▄ ██       │              │
│              │                            │              │
│              └────────────────────────────┘              │
│                                                          │
│                    Backup Code                           │
│                   ┌──────────┐                           │
│                   │ A7K9M2   │                           │
│                   └──────────┘                           │
│                                                          │
│              Show this to the host to                    │
│              redeem your experience                      │
│                                                          │
│              ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                   │
│              Tap anywhere to close                       │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

## Screen 9: Scanner Page

```
┌──────────────────────────────────────────────────────────┐
│  [Sidebar]  │                                            │
│             │  📷  Scan Ticket                            │
│             │  Scan QR code or enter backup code          │
│             │                                            │
│             │  ┌────────────────────────────────────┐    │
│             │  │                                    │    │
│             │  │                                    │    │
│             │  │         📷 Camera Preview           │    │
│             │  │                                    │    │
│             │  │      ┌──────────────────┐          │    │
│             │  │      │   Scanning...    │          │    │
│             │  │      │   Point camera   │          │    │
│             │  │      │   at QR code     │          │    │
│             │  │      └──────────────────┘          │    │
│             │  │                                    │    │
│             │  │                                    │    │
│             │  └────────────────────────────────────┘    │
│             │                                            │
│             │  ─── OR ───────────────────────────────    │
│             │                                            │
│             │  Enter Backup Code Manually                │
│             │  ┌─────────────────────┐                   │
│             │  │  e.g. A7K9M2        │  [ Verify ▸ ]    │
│             │  └─────────────────────┘                   │
│             │  6-character alphanumeric code              │
│             │                                            │
│             │  ─────────────────────────────────────     │
│             │                                            │
│             │  Recent Scans                              │
│             │  ┌────────────────────────────────────┐    │
│             │  │  ✅ Spa Day Package — K. Nordmann   │    │
│             │  │     Redeemed just now               │    │
│             │  └────────────────────────────────────┘    │
│             │  ┌────────────────────────────────────┐    │
│             │  │  ✅ Rock Climbing — P. Hansen       │    │
│             │  │     Redeemed 2 hours ago            │    │
│             │  └────────────────────────────────────┘    │
│             │                                            │
└──────────────────────────────────────────────────────────┘
```

**Camera Permission Denied Variant:**
```
│             │  ┌────────────────────────────────────┐    │
│             │  │  ⚠️ Camera access required          │    │
│             │  │                                    │    │
│             │  │  Please allow camera access in     │    │
│             │  │  your browser settings to scan     │    │
│             │  │  QR codes.                         │    │
│             │  │                                    │    │
│             │  │  [ 🔄 Retry Camera Access ]        │    │
│             │  └────────────────────────────────────┘    │
│             │                                            │
│             │  Or use manual code entry below:           │
```

---

## Screen 10: Scan Confirmation (Pre-Redemption)

```
┌─────────────────────────────────────────────────┐
│  🎫  Ticket Found!               ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  ✅ Valid ticket — ready to redeem               │
│                                                 │
│  EXPERIENCE                                     │
│  Spa Day Package                                │
│  💆 Wellness  ·  📍 Bergen                       │
│                                                 │
│  EMPLOYEE                                       │
│  Kari Nordmann                                  │
│                                                 │
│  REQUESTING COMPANY                             │
│  TechCorp AS                                    │
│                                                 │
│  POINTS                                         │
│  +50 points will be credited to your balance    │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│  ⚠️  This action cannot be undone.              │
│                                                 │
│    [ Cancel ]         [ ✅ Confirm Redemption ]  │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

## Screen 11: Redemption Success

```
┌─────────────────────────────────────────────────┐
│                                                 │
│                    ✅                            │
│                                                 │
│           Experience Redeemed!                  │
│                                                 │
│      +50 points credited to your balance        │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│  Experience: Spa Day Package                    │
│  Employee: Kari Nordmann                        │
│  Company: TechCorp AS                           │
│  Date: March 10, 2026                           │
│                                                 │
│  ─────────────────────────────────────────────  │
│                                                 │
│          [ 📷 Scan Another Ticket ]             │
│          [ ← Back to Bookings ]                 │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

## Screen 12: Ticket — Already Used / Error States

**Already Used:**
```
┌─────────────────────────────────────────────────┐
│  ⚠️  Ticket Already Redeemed     ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  This ticket was already redeemed on:           │
│  📅 March 8, 2026 at 14:15                      │
│                                                 │
│  Experience: Spa Day Package                    │
│  Employee: Kari Nordmann                        │
│  Company: TechCorp AS                           │
│                                                 │
│              [ Scan Another ]                   │
└─────────────────────────────────────────────────┘
```

**Invalid Code:**
```
┌─────────────────────────────────────────────────┐
│  ❌  Invalid Code                 ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  This code is not recognized. Please check      │
│  the code and try again.                        │
│                                                 │
│           [ Try Again ]                         │
└─────────────────────────────────────────────────┘
```

**Wrong Host:**
```
┌─────────────────────────────────────────────────┐
│  ⚠️  Wrong Experience             ✕ Close        │
│  ─────────────────────────────────────────────  │
│                                                 │
│  This ticket is for an experience hosted by     │
│  another company. Only the host can redeem it.  │
│                                                 │
│           [ Scan Another ]                      │
└─────────────────────────────────────────────────┘
```

---

## Status Badge Specifications (Feature 13)

| Status | Background | Text Color | Icon | Example |
|--------|-----------|------------|------|---------|
| Pending | `#FEF3C7` | `#92400E` | `fa-clock` | 🟡 Pending |
| Confirmed | `#DBEAFE` | `#1E40AF` | `fa-check-circle` | 🔵 Confirmed |
| Used | `#DCFCE7` | `#166534` | `fa-check-double` | 🟢 Used |
| Rejected | `#FEE2E2` | `#991B1B` | `fa-times-circle` | 🔴 Rejected |

---

## Navigation Updates

**Sidebar additions for M5:**

```
Main Menu:
  Dashboard
  Marketplace
  My Bookings          ← NEW (replaces nothing, new item)
    ├── Outgoing       (tab)
    └── Incoming       (tab)
  Points & Balance

Management:
  Employees
  Experiences
  📷 Scan Ticket       ← NEW (visible to Owner/Manager only)
  Tax Reports
  Settings
```

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 5 of 8
