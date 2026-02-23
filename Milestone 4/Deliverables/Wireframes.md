# SwapJoys Platform - Wireframes
## Milestone 4: Experience Creation & Marketplace (Features 4, 5)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 4 of 8 |
| **Features** | Create Experience (F4), Browse Experiences (F5) |
| **Prepared by** | Rebing Tech |
| **Date** | February 2026 |
| **Status** | Ready for Client Approval |

---

## Screen Overview

| # | Screen | Description | Actor |
|---|--------|-------------|-------|
| 1 | My Experiences | View company's own experiences | Owner/Manager |
| 2 | Create Experience | Form to create new experience | Owner/Manager |
| 3 | Edit Experience | Form to edit existing experience | Owner/Manager |
| 4 | Marketplace | Browse all available experiences | All Roles |
| 5 | Experience Detail | View full experience details | All Roles |
| 6 | Experience Detail (Owner) | Owner view with edit/deactivate | Owner/Manager |
| 7 | Empty State | No experiences created yet | Owner/Manager |

---

## Sidebar Navigation

### Owner/Manager View
```
┌──────────────────┐
│ [S] SwapJoys     │
│                  │
│ ─────────────    │
│                  │
│ MAIN MENU        │
│                  │
│ □ Dashboard      │
│ □ Marketplace    │
│                  │
│ ─────────────    │
│                  │
│ MANAGEMENT       │
│                  │
│ □ Employees      │
│ ■ Experiences ◄  │
│                  │
└──────────────────┘
```

### Employee View (Marketplace Only)
```
┌──────────────────┐
│ [S] SwapJoys     │
│                  │
│ ─────────────    │
│                  │
│ MAIN MENU        │
│                  │
│ □ Dashboard      │
│ ■ Marketplace ◄  │
│                  │
└──────────────────┘
```

---

## 1. My Experiences Page (Owner/Manager View)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    MY EXPERIENCES PAGE                           │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Experiences                              [+ Create Experience]  │
│                  │  Manage your company's experiences                                │
│ ─────────────    │                                                                  │
│                  │  ┌──────────┐  ┌──────────┐  ┌──────────┐                       │
│ MAIN MENU        │  │    8     │  │    6     │  │    2     │                       │
│                  │  │  Total   │  │  Active  │  │ Inactive │                       │
│ □ Dashboard      │  │Experiences│  │          │  │          │                       │
│ □ Marketplace    │  └──────────┘  └──────────┘  └──────────┘                       │
│                  │                                                                  │
│ ─────────────    │  ┌───────────────┐  ┌───────────────┐  ┌───────────────┐       │
│                  │  │ [  PHOTO  ]   │  │ [  PHOTO  ]   │  │ [  PHOTO  ]   │       │
│ MANAGEMENT       │  │               │  │               │  │               │       │
│                  │  │ Team Dinner   │  │ Spa Day       │  │ Movie Night   │       │
│ □ Employees      │  │ TechCorp AS   │  │ TechCorp AS   │  │ TechCorp AS   │       │
│ ■ Experiences ◄  │  │               │  │               │  │               │       │
│                  │  │ 🍽️ Dining     │  │ 💆 Wellness   │  │ 🎭 Entertain. │       │
│                  │  │ 📍 Oslo       │  │ 📍 Bergen     │  │ 📍 Trondheim  │       │
│                  │  │ 💰 30 points  │  │ 💰 50 points  │  │ 💰 20 points  │       │
│                  │  │               │  │               │  │               │       │
│                  │  │ [🟢 Active]   │  │ [🟢 Active]   │  │ [⚫ Inactive] │       │
│                  │  │               │  │               │  │               │       │
│                  │  │ [✏️ Edit] [👁] │  │ [✏️ Edit] [👁] │  │ [✏️ Edit] [👁] │       │
│                  │  └───────────────┘  └───────────────┘  └───────────────┘       │
│                  │                                                                  │
│                  │  ┌───────────────┐  ┌───────────────┐  ┌───────────────┐       │
│                  │  │  ...more      │  │  ...more      │  │  ...more      │       │
│                  │  └───────────────┘  └───────────────┘  └───────────────┘       │
│                  │                                                                  │
│                  │                    [1] [2] [Next →]                              │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Stats Cards | Total, Active, Inactive experience counts |
| Experience Cards | Grid of 3 per row with photo, title, company, category, city, points, status |
| Status Badge | Active (green), Inactive (gray) |
| Actions | Edit, View on each card |
| Pagination | Page numbers at bottom |

---

## 2. Create Experience Form

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    CREATE EXPERIENCE PAGE                        │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  ← Create Experience                                             │
│                  │  Fill in the details to publish your experience                   │
│ ─────────────    │                                                                  │
│                  │  ┌─────────────────────────────────────────────────────────────┐ │
│ MAIN MENU        │  │                                                             │ │
│                  │  │  Experience Title *                                         │ │
│ □ Dashboard      │  │  ┌─────────────────────────────────────────────────┐       │ │
│ □ Marketplace    │  │  │ e.g. Team Dinner at Restaurant X                │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│ ─────────────    │  │                                                             │ │
│                  │  │  Description *                                              │ │
│ MANAGEMENT       │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │                                                  │       │ │
│ □ Employees      │  │  │ Describe the experience in detail...            │       │ │
│ ■ Experiences ◄  │  │  │                                                  │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│                  │  │                                                             │ │
│                  │  │  Photo *                                                    │ │
│                  │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │                                                  │       │ │
│                  │  │  │     📷  Click to upload or drag & drop          │       │ │
│                  │  │  │         JPG or PNG, max 5MB                     │       │ │
│                  │  │  │                                                  │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Capacity *            │  │ Point Cost *         │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ e.g. 10          │ │  │ │ e.g. 30          │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Category *            │  │ City *               │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ Select category ▼│ │  │ │ Select city    ▼ │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  ─── Tax Documentation Fields ────────────────────────      │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Estimated Value *     │  │ Welfare Benefit? *   │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ NOK 0.00         │ │  │ │ Select Yes/No  ▼ │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  │ ℹ️ Market value for  │  │ ℹ️ Does this qualify │        │ │
│                  │  │  │   tax purposes       │  │   as a welfare       │        │ │
│                  │  │  │                      │  │   benefit?           │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  Rules / Terms (Optional)                                   │ │
│                  │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │ Any special rules or conditions...              │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│                  │  │                                                             │ │
│                  │  │  ─────────────────────────────────────────────────────      │ │
│                  │  │                                                             │ │
│                  │  │                    [Cancel]  [🚀 Publish Experience]        │ │
│                  │  │                                                             │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Title Field | Required, min 3 characters |
| Description Field | Required, textarea, min 20 characters |
| Photo Upload | Drag & drop or click, JPG/PNG, max 5MB |
| Capacity Field | Required, positive integer |
| Point Cost Field | Required, positive integer |
| Category Dropdown | Required, predefined list |
| City Dropdown | Required, Norwegian cities |
| Estimated Value (NOK) | Required, for tax documentation (Feature 15 prep) |
| Welfare Classification | Required, Yes/No (Feature 16 prep) |
| Rules Field | Optional, textarea |
| Buttons | Cancel, Publish Experience |

---

## 3. Edit Experience Form

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    EDIT EXPERIENCE PAGE                          │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  ← Edit Experience                                               │
│                  │                                                                  │
│ ─────────────    │  ┌─────────────────────────────────────────────────────────────┐ │
│                  │  │                                                             │ │
│ MAIN MENU        │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │ [Current Photo Preview]                         │       │ │
│ □ Dashboard      │  │  │                                                 │       │ │
│ □ Marketplace    │  │  │              📷 Change Photo                    │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│ ─────────────    │  │                                                             │ │
│                  │  │  Experience Title *                                         │ │
│ MANAGEMENT       │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │ Team Dinner at Restaurant X                      │       │ │
│ □ Employees      │  │  └─────────────────────────────────────────────────┘       │ │
│ ■ Experiences ◄  │  │                                                             │ │
│                  │  │  Description *                                              │ │
│                  │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │ Enjoy a wonderful team dinner experience...      │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Capacity *            │  │ Point Cost *         │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ 10               │ │  │ │ 30               │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Category *            │  │ City *               │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ Dining         ▼ │ │  │ │ Oslo           ▼ │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  ─── Tax Documentation Fields ────────────────────────      │ │
│                  │  │                                                             │ │
│                  │  │  ┌──────────────────────┐  ┌──────────────────────┐        │ │
│                  │  │  │ Estimated Value *     │  │ Welfare Benefit? *   │        │ │
│                  │  │  │ ┌──────────────────┐ │  │ ┌──────────────────┐ │        │ │
│                  │  │  │ │ NOK 500.00       │ │  │ │ Yes            ▼ │ │        │ │
│                  │  │  │ └──────────────────┘ │  │ └──────────────────┘ │        │ │
│                  │  │  └──────────────────────┘  └──────────────────────┘        │ │
│                  │  │                                                             │ │
│                  │  │  Rules / Terms (Optional)                                   │ │
│                  │  │  ┌─────────────────────────────────────────────────┐       │ │
│                  │  │  │ Maximum 10 people per session                    │       │ │
│                  │  │  └─────────────────────────────────────────────────┘       │ │
│                  │  │                                                             │ │
│                  │  │  ─────────────────────────────────────────────────────      │ │
│                  │  │                                                             │ │
│                  │  │        [Cancel]  [💾 Save Changes]  [🚫 Deactivate]        │ │
│                  │  │                                                             │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Photo Preview | Current photo with change option |
| All Form Fields | Pre-filled with existing data |
| Buttons | Cancel, Save Changes, Deactivate |

---

## 4. Marketplace Page (Browse Experiences)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    MARKETPLACE PAGE                              │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Marketplace                                                     │
│                  │  Discover experiences from other companies                        │
│ ─────────────    │                                                                  │
│                  │  ┌─────────────────────────────────────────────────────────────┐ │
│ MAIN MENU        │  │                                                             │ │
│                  │  │ [🔍 Search experiences...  ]  [All Categories ▼] [All Cities ▼] │ │
│ □ Dashboard      │  │                                                             │ │
│ ■ Marketplace ◄  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
│ ─────────────    │  Showing 24 experiences                                          │
│                  │                                                                  │
│ MANAGEMENT       │  ┌───────────────┐  ┌───────────────┐  ┌───────────────┐       │
│                  │  │ [   PHOTO   ] │  │ [   PHOTO   ] │  │ [   PHOTO   ] │       │
│ □ Employees      │  │               │  │               │  │               │       │
│ □ Experiences    │  │ Yoga Classes  │  │ Wine Tasting  │  │ Rock Climbing │       │
│                  │  │ 🏢 HealthCo   │  │ 🏢 VinoAS     │  │ 🏢 AdventureCo│       │
│                  │  │               │  │               │  │               │       │
│                  │  │ 💆 Wellness   │  │ 🍽️ Dining     │  │ 🏃 Activities │       │
│                  │  │ 📍 Oslo       │  │ 📍 Bergen     │  │ 📍 Trondheim  │       │
│                  │  │               │  │               │  │               │       │
│                  │  │ 💰 40 points  │  │ 💰 60 points  │  │ 💰 35 points  │       │
│                  │  │               │  │               │  │               │       │
│                  │  │ [  View Details  ]│  │ [  View Details  ]│  │ [  View Details  ]│       │
│                  │  └───────────────┘  └───────────────┘  └───────────────┘       │
│                  │                                                                  │
│                  │  ┌───────────────┐  ┌───────────────┐  ┌───────────────┐       │
│                  │  │  ...more      │  │  ...more      │  │  ...more      │       │
│                  │  └───────────────┘  └───────────────┘  └───────────────┘       │
│                  │                                                                  │
│                  │                    [1] [2] [3] ... [Next →]                      │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Search Box | Search by title or company name |
| Category Filter | Dropdown with all categories |
| City Filter | Dropdown with Norwegian cities |
| Results Count | "Showing X experiences" |
| Experience Cards | Grid of 3 per row: Photo, Title, Company, Category, City, Points |
| View Details Button | Navigate to experience detail |
| Pagination | Page numbers at bottom |

---

## 5. Experience Detail Page (Marketplace View)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    EXPERIENCE DETAIL PAGE                        │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  ← Back to Marketplace                                           │
│                  │                                                                  │
│ ─────────────    │  ┌───────────────────────────────────────────────────┐           │
│                  │  │                                                   │           │
│ MAIN MENU        │  │                   [  LARGE PHOTO  ]              │           │
│                  │  │                                                   │           │
│ □ Dashboard      │  │                                                   │           │
│ ■ Marketplace ◄  │  └───────────────────────────────────────────────────┘           │
│                  │                                                                  │
│ ─────────────    │  ┌───────────────────────────────────────────────────┐           │
│                  │  │                                                   │           │
│ MANAGEMENT       │  │  Yoga Classes for Teams                          │           │
│                  │  │                                                   │           │
│ □ Employees      │  │  [💆 Wellness]  [📍 Oslo]                        │           │
│ □ Experiences    │  │                                                   │           │
│                  │  │  ─────────────────────────────────────────────    │           │
│                  │  │                                                   │           │
│                  │  │  Description                                      │           │
│                  │  │  A wonderful yoga experience for your team...     │           │
│                  │  │  Perfect for team building and wellness.          │           │
│                  │  │                                                   │           │
│                  │  │  ─────────────────────────────────────────────    │           │
│                  │  │                                                   │           │
│                  │  │  ┌───────────────┐  ┌───────────────┐            │           │
│                  │  │  │ POINT COST    │  │ CAPACITY      │            │           │
│                  │  │  │ 💰 40 points  │  │ 👥 8/10 left  │            │           │
│                  │  │  └───────────────┘  └───────────────┘            │           │
│                  │  │                                                   │           │
│                  │  │  ┌───────────────┐  ┌───────────────┐            │           │
│                  │  │  │ EST. VALUE    │  │ WELFARE       │            │           │
│                  │  │  │ 💵 NOK 800    │  │ ✅ Yes         │            │           │
│                  │  │  └───────────────┘  └───────────────┘            │           │
│                  │  │                                                   │           │
│                  │  │  ─────────────────────────────────────────────    │           │
│                  │  │                                                   │           │
│                  │  │  Rules & Terms                                    │           │
│                  │  │  • Maximum 10 people per session                  │           │
│                  │  │  • Must book at least 3 days in advance           │           │
│                  │  │                                                   │           │
│                  │  │  ─────────────────────────────────────────────    │           │
│                  │  │                                                   │           │
│                  │  │  🏢 Hosted by                                     │           │
│                  │  │  ┌─────────────────────────────────────────┐     │           │
│                  │  │  │  [HC]  HealthCo AS                      │     │           │
│                  │  │  │        Oslo, Norway                      │     │           │
│                  │  │  └─────────────────────────────────────────┘     │           │
│                  │  │                                                   │           │
│                  │  │       [ 🎫 Request Experience ]                   │           │
│                  │  │                                                   │           │
│                  │  └───────────────────────────────────────────────────┘           │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | "← Back to Marketplace" |
| Large Photo | Full-width experience photo |
| Title | Experience title prominent |
| Badges | Category badge, City badge |
| Description | Full experience description |
| Point Cost | Points required to book |
| Capacity | Remaining / Total capacity |
| Estimated Value | NOK value for tax |
| Welfare Tag | Yes/No badge |
| Rules | Experience rules/terms |
| Host Company | Company name and location |
| Request Button | "Request Experience" (M5 functionality) |

---

## 6. Experience Detail (Owner View)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    EXPERIENCE DETAIL (OWNER VIEW)                │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  ← Back to My Experiences                                        │
│                  │                                                                  │
│                  │  ┌───────────────────────────────────────────────────┐           │
│                  │  │                   [  LARGE PHOTO  ]              │           │
│                  │  └───────────────────────────────────────────────────┘           │
│                  │                                                                  │
│                  │  ┌───────────────────────────────────────────────────┐           │
│                  │  │                                                   │           │
│                  │  │  Team Dinner at Restaurant X       [🟢 Active]   │           │
│                  │  │                                                   │           │
│                  │  │  [🍽️ Dining]  [📍 Oslo]                          │           │
│                  │  │                                                   │           │
│                  │  │  (... same detail fields as marketplace view ...) │           │
│                  │  │                                                   │           │
│                  │  │  ─────────────────────────────────────────────    │           │
│                  │  │                                                   │           │
│                  │  │  [✏️ Edit]  [🚫 Deactivate]                       │           │
│                  │  │                                                   │           │
│                  │  └───────────────────────────────────────────────────┘           │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | "← Back to My Experiences" |
| Status Badge | Active (green) or Inactive (gray) on title row |
| All Detail Fields | Same as marketplace view |
| Edit Button | Navigate to edit form |
| Deactivate Button | Toggle experience visibility |

---

## 7. Empty State (No Experiences)

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│ SIDEBAR          │                    MY EXPERIENCES PAGE                           │
│ ───────────────  │ ─────────────────────────────────────────────────────────────── │
│                  │                                                                  │
│ [S] SwapJoys     │  Experiences                              [+ Create Experience]  │
│                  │  Manage your company's experiences                                │
│ ─────────────    │                                                                  │
│                  │  ┌─────────────────────────────────────────────────────────────┐ │
│ MAIN MENU        │  │                                                             │ │
│                  │  │                                                             │ │
│ □ Dashboard      │  │                         🎭                                  │ │
│ □ Marketplace    │  │                                                             │ │
│                  │  │                  No Experiences Yet                          │ │
│ ─────────────    │  │                                                             │ │
│                  │  │     Create your first experience and start sharing           │ │
│ MANAGEMENT       │  │           with other companies on SwapJoys.                 │ │
│                  │  │                                                             │ │
│ □ Employees      │  │              [+ Create Your First Experience]               │ │
│ ■ Experiences ◄  │  │                                                             │ │
│                  │  │                                                             │ │
│                  │  └─────────────────────────────────────────────────────────────┘ │
│                  │                                                                  │
└──────────────────┴──────────────────────────────────────────────────────────────────┘
```

### Elements

| Element | Description |
|---------|-------------|
| Icon | Large theater/experience icon (gray) |
| Title | "No Experiences Yet" |
| Message | Encouraging text |
| CTA Button | "Create Your First Experience" |

---

## Component Specifications

### Experience Card (Grid)

| Element | Description |
|---------|-------------|
| Photo | 280×180px area, rounded corners |
| Title | Bold, max 2 lines |
| Company Name | With building icon |
| Category | Badge with icon |
| City | With location pin icon |
| Point Cost | With coin icon |
| Status | Active/Inactive badge (My Experiences only) |

### Category Badges

| Category | Icon | Color |
|----------|------|-------|
| Dining | 🍽️ | Orange (#f97316) |
| Wellness | 💆 | Green (#22c55e) |
| Entertainment | 🎭 | Purple (#a855f7) |
| Activities | 🏃 | Blue (#3b82f6) |
| Culture | 🎨 | Pink (#ec4899) |
| Travel | ✈️ | Indigo (#6366f1) |
| Other | 📦 | Gray (#6b7280) |

### Status Badges

| Status | Color |
|--------|-------|
| Active | Green (#16a34a) |
| Inactive | Gray (#6b7280) |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 4 of 8
