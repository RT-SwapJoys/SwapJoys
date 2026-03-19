# SwapJoys Platform - Wireframes
## Milestone 6: Points System & Balance (Features 8, 9, 10)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 6 of 8 |
| **Features** | Simple Fixed-Point System (F8), Company Balance Overview (F9), Admin Override (F10) |
| **Prepared by** | Rebing Tech |
| **Date** | March 2026 |
| **Status** | Ready for Client Approval |

---

## Screen Overview

| # | Screen | Description | Actor |
|---|--------|-------------|-------|
| 1 | Points & Balance Dashboard | Balance summary, earned/spent, recent transactions | Owner/Manager |
| 2 | Transaction History | Full list of all point movements with filters | Owner/Manager |
| 3 | Transaction Detail | Detailed view of a single transaction | Owner/Manager |
| 4 | Admin - Point Adjustments | Company list with balances, adjustment form | SwapJoys Admin |
| 5 | Admin - Adjustment Confirmation | Confirmation dialog before processing | SwapJoys Admin |
| 6 | Admin - Adjustment History | Audit trail of all admin adjustments | SwapJoys Admin |
| 7 | Admin - Adjustment Detail | Full detail view of single adjustment | SwapJoys Admin |

---

## 1. Points & Balance Dashboard (Owner/Manager View)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                 POINTS & BALANCE DASHBOARD                      │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Points & Balance                                               │
│                  │  Track your company's point activity and balance                 │
│ ─────────────    │                                                                  │
│                  │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ MAIN MENU        │  │   💰 1,250    │  │   📥 2,450   │  │   📤 1,200   │  │   ⏳ 150     │
│                  │  │              │  │              │  │              │  │              │
│ □ Dashboard      │  │   Current    │  │   Points     │  │   Points     │  │   Pending    │
│ □ Marketplace    │  │   Balance    │  │   Earned     │  │   Spent      │  │   Bookings   │
│ □ My Bookings    │  │              │  │              │  │              │  │              │
│ ■ Points &       │  └──────────────┘  └──────────────┘  └──────────────┘  └──────────────┘
│   Balance ◄      │                                                                  │
│ □ Employees      │  ┌─────────────────────────────────────────────────────────────┐ │
│ □ Experiences    │  │ Recent Transactions                    [View All →]         │ │
│ □ Tax Reports    │  ├─────────────────────────────────────────────────────────────┤ │
│ □ Settings       │  │                                                             │ │
│                  │  │ DATE        │ TYPE           │ DESCRIPTION      │ POINTS    │ │
│                  │  │ ────────────┼────────────────┼──────────────────┼────────── │ │
│                  │  │ Mar 17      │ 📥 Credit      │ Spa Day redeemed │ +50       │ │
│                  │  │             │                │ from Nordic AS   │  🟢       │ │
│                  │  │ ────────────┼────────────────┼──────────────────┼────────── │ │
│                  │  │ Mar 15      │ 📤 Deduction   │ Team Lunch       │ -30       │ │
│                  │  │             │                │ to FoodCorp AS   │  🔴       │ │
│                  │  │ ────────────┼────────────────┼──────────────────┼────────── │ │
│                  │  │ Mar 12      │ ⚙️ Adjustment  │ Admin: Bonus     │ +100      │ │
│                  │  │             │                │ credit           │  🟢       │ │
│                  │  │ ────────────┼────────────────┼──────────────────┼────────── │ │
│                  │  │ Mar 10      │ 📤 Deduction   │ Gym Session      │ -25       │ │
│                  │  │             │                │ to FitNord AS    │  🔴       │ │
│                  │  │ ────────────┼────────────────┼──────────────────┼────────── │ │
│                  │  │ Jan 15      │ 🎁 Welcome     │ Registration     │ +50       │ │
│                  │  │             │                │ bonus            │  🟢       │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Current Balance Card | Large number, primary color, prominent display |
| Points Earned Card | Total credits, green accent |
| Points Spent Card | Total debits, orange/red accent |
| Pending Bookings Card | Points reserved for pending bookings |
| Recent Transactions | Last 5–10 entries with type icons and +/- indicators |
| View All Link | Navigate to full Transaction History |

---

## 2. Transaction History Page

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                  TRANSACTION HISTORY                             │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Transaction History                         [← Back to Points] │
│                  │  Complete history of all point movements                         │
│                  │                                                                  │
│ ■ Points &       │  ┌─────────────────────────────────────────────────────────────┐ │
│   Balance ◄      │  │                                                             │ │
│                  │  │ [🔍 Search...         ]  [All Types ▼]  [Date Range 📅]     │ │
│                  │  │                                                             │ │
│                  │  │ ┌───────────────────────────────────────────────────────────┐│ │
│                  │  │ │ DATE     │ TYPE       │ DESCRIPTION    │ POINTS │ BAL.   ││ │
│                  │  │ ├───────────────────────────────────────────────────────────┤│ │
│                  │  │ │ Mar 17   │ 📥 Credit  │ Spa Day        │ +50    │ 1,250  ││ │
│                  │  │ │ 14:30    │            │ Nordic Well AS │        │        ││ │
│                  │  │ ├───────────────────────────────────────────────────────────┤│ │
│                  │  │ │ Mar 15   │ 📤 Debit   │ Team Lunch     │ -30    │ 1,200  ││ │
│                  │  │ │ 10:15    │            │ FoodCorp AS    │        │        ││ │
│                  │  │ ├───────────────────────────────────────────────────────────┤│ │
│                  │  │ │ Mar 12   │ ⚙️ Admin   │ Bonus credit   │ +100   │ 1,230  ││ │
│                  │  │ │ 09:00    │            │ SwapJoys Admin │        │        ││ │
│                  │  │ ├───────────────────────────────────────────────────────────┤│ │
│                  │  │ │ Mar 10   │ 📤 Debit   │ Gym Session    │ -25    │ 1,130  ││ │
│                  │  │ │ 11:45    │            │ FitNord AS     │        │        ││ │
│                  │  │ ├───────────────────────────────────────────────────────────┤│ │
│                  │  │ │ Mar 05   │ 📥 Credit  │ Cooking Class  │ +35    │ 1,155  ││ │
│                  │  │ │ 16:20    │            │ TechCorp AS    │        │        ││ │
│                  │  │ └───────────────────────────────────────────────────────────┘│ │
│                  │  │                                                             │ │
│                  │  │                  [1] [2] [3] ... [Next →]                   │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Search Box | Filter by experience name or company name |
| Type Filter | All, Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment |
| Date Range | Start date / End date picker |
| Transaction Table | Date/Time, Type (icon), Description, Points (+/-), Balance After |
| Row Click | Navigate to Transaction Detail |
| Pagination | 20 transactions per page |

---

## 3. Transaction Detail

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                                                         │   │
│  │  ← Back to Transaction History                          │   │
│  │                                                         │   │
│  │  Transaction Detail                                     │   │
│  │  ─────────────────────────────────────────────────────  │   │
│  │                                                         │   │
│  │  ┌─────────────────────────────────────────────────┐   │   │
│  │  │  📥 Redemption Credit            +50 points     │   │   │
│  │  │                                    🟢            │   │   │
│  │  └─────────────────────────────────────────────────┘   │   │
│  │                                                         │   │
│  │  Transaction ID       TXN-2026-0342                     │   │
│  │  Date & Time          March 17, 2026 at 14:30           │   │
│  │  Type                 Redemption Credit                  │   │
│  │  Experience           Spa Day Package                    │   │
│  │  Points               +50                                │   │
│  │  Balance Before       1,200                              │   │
│  │  Balance After        1,250                              │   │
│  │  Other Party          Nordic Wellness AS                 │   │
│  │  Notes                Ticket SPA7K2 redeemed             │   │
│  │                                                         │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | Return to Transaction History |
| Type Header | Icon + type name + points amount with color |
| Detail Fields | Transaction ID, Date/Time, Type, Experience, Points, Balance Before/After, Other Party, Notes |

---

## 4. Admin - Point Adjustments Page

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ ADMIN SIDEBAR    │                  POINT ADJUSTMENTS                               │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Point Adjustments                                              │
│    ADMIN         │  Manually adjust company point balances                          │
│                  │                                                                  │
│ ─────────────    │  [Adjustments]  [Adjustment History]                             │
│                  │                                                                  │
│ □ Dashboard      │  ┌─────────────────────────────────────────────────────────────┐ │
│ □ Companies      │  │                                                             │ │
│ □ Experiences    │  │ [🔍 Search companies...                               ]     │ │
│ □ Usage Logs     │  │                                                             │ │
│ ■ Point          │  │ ┌───────────────────────────────────────────────────────┐   │ │
│   Adjustments ◄  │  │ │ COMPANY            │ ORG #     │ STATUS  │ BALANCE   │   │ │
│ □ Settings       │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ TechCorp AS        │ 912345678 │ 🟢 Active│ 1,250    │   │ │
│                  │  │ │                    │           │         │ [Adjust]  │   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ Nordic Wellness AS │ 923456789 │ 🟢 Active│ 830      │   │ │
│                  │  │ │                    │           │         │ [Adjust]  │   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ FoodCorp AS        │ 934567890 │ 🟢 Active│ 420      │   │ │
│                  │  │ │                    │           │         │ [Adjust]  │   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ FitNord AS         │ 945678901 │ 🟢 Active│ 95       │   │ │
│                  │  │ │                    │           │         │ [Adjust]  │   │ │
│                  │  │ └───────────────────────────────────────────────────────┘   │ │
│                  │  │                                                             │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Tabs | Adjustments / Adjustment History |
| Search Box | Filter companies by name |
| Company Table | Company Name, Org Number, Status, Current Balance, Adjust Button |
| Adjust Button | Opens adjustment modal/form |

---

## 5. Admin - Adjustment Form Modal

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   ┌─────────────────────────────────────────────────────────┐   │
│   │                                                         │   │
│   │  ⚙️ Adjust Points                                [✕]   │   │
│   │  ─────────────────────────────────────────────────────  │   │
│   │                                                         │   │
│   │  Company                                                │   │
│   │  ┌─────────────────────────────────────────────────┐   │   │
│   │  │ TechCorp AS                                      │   │   │
│   │  └─────────────────────────────────────────────────┘   │   │
│   │                                                         │   │
│   │  Current Balance: 1,250 points                          │   │
│   │                                                         │   │
│   │  Adjustment Type *                                      │   │
│   │  ┌─────────────────────────────────────────────────┐   │   │
│   │  │  ◉ Add Points    ○ Remove Points             ▼  │   │   │
│   │  └─────────────────────────────────────────────────┘   │   │
│   │                                                         │   │
│   │  Amount *                                               │   │
│   │  ┌─────────────────────────────────────────────────┐   │   │
│   │  │ 100                                              │   │   │
│   │  └─────────────────────────────────────────────────┘   │   │
│   │                                                         │   │
│   │  New Balance Preview: 1,350 points                      │   │
│   │                                                         │   │
│   │  Reason *                                               │   │
│   │  ┌─────────────────────────────────────────────────┐   │   │
│   │  │ Promotional bonus for pilot participation       │   │   │
│   │  │                                                  │   │   │
│   │  │                                                  │   │   │
│   │  └─────────────────────────────────────────────────┘   │   │
│   │  Min 10 characters                                      │   │
│   │                                                         │   │
│   │  ─────────────────────────────────────────────────────  │   │
│   │                                                         │   │
│   │              [Cancel]    [Apply Adjustment]              │   │
│   │                                                         │   │
│   └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Company Display | Read-only, shows selected company |
| Current Balance | Display current balance |
| Adjustment Type | Radio: Add Points / Remove Points |
| Amount Field | Positive integer input |
| New Balance Preview | Live calculation: Current ± Amount |
| Reason Textarea | Mandatory, min 10 characters |
| Cancel Button | Close modal, discard |
| Apply Button | Submit adjustment |

---

## 6. Admin - Adjustment History

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ ADMIN SIDEBAR    │                  ADJUSTMENT HISTORY                              │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Point Adjustments                                              │
│    ADMIN         │  Audit trail of all admin point adjustments                      │
│                  │                                                                  │
│ ■ Point          │  [Adjustments]  [Adjustment History ◄]                           │
│   Adjustments ◄  │                                                                  │
│                  │  ┌─────────────────────────────────────────────────────────────┐ │
│                  │  │                                                             │ │
│                  │  │ [All Companies ▼]  [All Types ▼]  [Date Range 📅]          │ │
│                  │  │                                                             │ │
│                  │  │ ┌───────────────────────────────────────────────────────┐   │ │
│                  │  │ │ DATE    │ ADMIN     │ COMPANY    │ TYPE │ AMT  │REASON│   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ Mar 12  │ Admin     │ TechCorp   │ ➕   │ +100 │Bonus │   │ │
│                  │  │ │ 09:00   │ Selim     │ AS         │ Add  │      │cre.. │   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ Mar 08  │ Admin     │ FitNord    │ ➕   │ +50  │Pilot │   │ │
│                  │  │ │ 14:20   │ Selim     │ AS         │ Add  │      │par.. │   │ │
│                  │  │ ├───────────────────────────────────────────────────────┤   │ │
│                  │  │ │ Feb 28  │ Admin     │ Nordic     │ ➖   │ -20  │Corr  │   │ │
│                  │  │ │ 11:30   │ Selim     │ Well. AS   │ Rem  │      │ect.. │   │ │
│                  │  │ └───────────────────────────────────────────────────────┘   │ │
│                  │  │                                                             │ │
│                  │  │                  [1] [2] ... [Next →]                       │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Tabs | Adjustments / Adjustment History (active) |
| Company Filter | Dropdown of all companies |
| Type Filter | All, Add, Remove |
| Date Range | Start/End date picker |
| Table Columns | Date, Admin Name, Company, Type, Amount, Reason (truncated) |
| Row Click | Navigate to full adjustment detail |
| Pagination | 20 entries per page |

---

## 7. Admin - Adjustment Detail

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                                                         │   │
│  │  ← Back to Adjustment History                           │   │
│  │                                                         │   │
│  │  Adjustment Detail                                      │   │
│  │  ─────────────────────────────────────────────────────  │   │
│  │                                                         │   │
│  │  ┌─────────────────────────────────────────────────┐   │   │
│  │  │  ⚙️ Admin Adjustment (Add)        +100 points   │   │   │
│  │  │                                      🟢          │   │   │
│  │  └─────────────────────────────────────────────────┘   │   │
│  │                                                         │   │
│  │  Adjustment ID        ADJ-2026-0015                     │   │
│  │  Date & Time          March 12, 2026 at 09:00           │   │
│  │  Admin                Admin Selim                        │   │
│  │  Company              TechCorp AS                        │   │
│  │  Type                 Add Points                         │   │
│  │  Amount               +100 points                        │   │
│  │  Balance Before       1,130                              │   │
│  │  Balance After        1,230                              │   │
│  │                                                         │   │
│  │  Reason                                                 │   │
│  │  ┌─────────────────────────────────────────────────┐   │   │
│  │  │ Promotional bonus for pilot participation.       │   │   │
│  │  │ Company joined as early adopter.                 │   │   │
│  │  └─────────────────────────────────────────────────┘   │   │
│  │                                                         │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | Return to Adjustment History |
| Type Header | Icon + type + amount with color indicator |
| Detail Fields | Adjustment ID, Date/Time, Admin, Company, Type, Amount, Balance Before/After |
| Reason Box | Full reason text in styled container |

---

## Component Specifications

### Transaction Type Icons

| Type | Icon | Color | Badge |
|------|------|-------|-------|
| Welcome Bonus | 🎁 Gift | Green (#16a34a) | Green background |
| Booking Deduction | 📤 Outbox | Red (#dc2626) | Red background |
| Redemption Credit | 📥 Inbox | Green (#16a34a) | Green background |
| Admin Add | ⚙️ Gear | Green (#16a34a) | Green background |
| Admin Remove | ⚙️ Gear | Red (#dc2626) | Red background |

### Points Display Colors

| Points | Color | Indicator |
|--------|-------|-----------|
| Positive (+) | Green (#16a34a) | 🟢 or ▲ |
| Negative (−) | Red (#dc2626) | 🔴 or ▼ |
| Zero / Neutral | Gray (#6b7280) | — |

### Balance Card Colors

| Card | Icon Color | Background |
|------|------------|------------|
| Current Balance | Blue (#6366f1) | Light blue |
| Points Earned | Green (#22c55e) | Light green |
| Points Spent | Orange (#f97316) | Light orange |
| Pending Bookings | Purple (#a855f7) | Light purple |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 6 of 8
