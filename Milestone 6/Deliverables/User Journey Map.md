# SwapJoys Platform - User Journey Map
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

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Points & Balance Dashboard | View company points balance and transaction overview | Owner/Manager |
| Phase 2 | Transaction History | View detailed history of all point movements | Owner/Manager |
| Phase 3 | Points Display Across Platform | See points on experience cards and detail pages | All Roles |
| Phase 4 | SwapJoys Admin - Point Adjustments | Manually adjust company point balances | SwapJoys Admin |
| Phase 5 | SwapJoys Admin - Adjustment History | View audit trail of all admin adjustments | SwapJoys Admin |

---

## Phase 1: Points & Balance Dashboard

**Goal:** Owner/Manager views their company's current points balance and transaction overview

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | User clicks "Points & Balance" in sidebar | Navigate to Points & Balance dashboard |
| 1.2 | — | Load company points data |
| 1.3 | — | Display Current Balance prominently (large number) |
| 1.4 | — | Display Points Earned total (sum of all credits) |
| 1.5 | — | Display Points Spent total (sum of all debits) |
| 1.6 | — | Calculate balance: Earned − Spent = Current Balance |
| 1.7 | User views balance summary cards | Show 4 cards: Current Balance, Points Earned, Points Spent, Pending Bookings |
| 1.8 | — | Display Recent Transactions list (last 5–10 transactions) |
| 1.9 | User sees transaction entries | Each entry shows: Date, Type, Experience, Points (+/-), Other Party |
| 1.10 | User clicks "View All Transactions" | Navigate to full Transaction History page |

**Success Criteria:**
- Current balance calculated correctly (Earned − Spent)
- Balance summary cards display accurate totals
- Recent transactions displayed with correct details
- All point movements from bookings, redemptions, welcome bonus, and admin adjustments included

---

## Phase 2: Transaction History

**Goal:** Owner/Manager views detailed history of all company point movements

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | User clicks "View All Transactions" or "Transaction History" tab | Navigate to Transaction History page |
| 2.2 | — | Load all transactions for company from points ledger |
| 2.3 | — | Display transactions in table format (newest first) |
| 2.4 | User sees transaction columns | Show: Date, Type, Description, Points (+/-), Balance After, Other Party |
| 2.5 | User filters by type | Show dropdown: All, Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment |
| 2.6 | User filters by date range | Select start and end date |
| 2.7 | User searches transactions | Search by experience name or company name |
| 2.8 | User views a specific transaction | Click row to see full transaction detail |
| 2.9 | — | Display: Transaction ID, Date/Time, Type, Experience, Points, Balance Before, Balance After, Other Party, Notes |
| 2.10 | User navigates pagination | Display 20 transactions per page |

**Transaction Types:**

| Type | Icon | Points | Description |
|------|------|--------|-------------|
| Welcome Bonus | 🎁 | +50 | Awarded on company registration |
| Booking Deduction | 📤 | −X | Points deducted when booking is approved |
| Redemption Credit | 📥 | +X | Points credited when ticket is redeemed |
| Admin Adjustment (Credit) | ⚙️ | +X | Admin added points to company |
| Admin Adjustment (Debit) | ⚙️ | −X | Admin removed points from company |

**Success Criteria:**
- All transactions displayed with correct details
- Filters work individually and in combination
- Pagination working for large transaction lists
- Points ledger is append-only (immutable)
- Balance After is calculated correctly for each entry

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No transactions | "No transactions found" | Show empty state with message |
| No filter results | "No transactions match your filters" | Show clear filters button |

---

## Phase 3: Points Display Across Platform

**Goal:** Users see point values and balance indicators throughout the platform

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | User views experience cards in marketplace | Display point cost on each card |
| 3.2 | User views experience detail page | Display point cost prominently |
| 3.3 | User initiates booking request | Show company balance and experience cost |
| 3.4 | — | Display "Sufficient" or "Insufficient" points indicator |
| 3.5 | User views dashboard | Display current balance in header or summary card |
| 3.6 | User views My Bookings | Show points deducted/credited per booking |
| 3.7 | User views ticket after redemption | Show points that were credited to host |

**Success Criteria:**
- Points visible on all experience cards in marketplace
- Balance visible on dashboard and in header area
- Insufficient balance clearly indicated before booking

---

## Phase 4: SwapJoys Admin - Point Adjustments

**Goal:** SwapJoys platform admin manually adjusts a company's point balance

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | Admin logs into SwapJoys Admin panel | Display Admin Dashboard |
| 4.2 | Admin clicks "Point Adjustments" in admin sidebar | Navigate to Point Adjustments page |
| 4.3 | — | Display list of all companies with current balances |
| 4.4 | Admin searches for a company | Filter company list by name |
| 4.5 | Admin selects a company | Highlight selected company, show current balance |
| 4.6 | Admin clicks "Adjust Points" | Open adjustment form |
| 4.7 | Admin selects adjustment type | Choose: Add Points / Remove Points |
| 4.8 | Admin enters point amount | Validate positive integer |
| 4.9 | Admin enters reason (mandatory) | Validate minimum 10 characters |
| 4.10 | Admin clicks "Apply Adjustment" | Show confirmation dialog |
| 4.11 | Admin confirms adjustment | Validate all fields |
| 4.12 | — | Update company points balance |
| 4.13 | — | Create points ledger entry (append-only) |
| 4.14 | — | Create admin audit log entry |
| 4.15 | — | Show success message with new balance |
| 4.16 | — | Return to company list with updated balance |

**Validation Rules:**

| Field | Rules |
|-------|-------|
| Company | Required, must select from list |
| Adjustment Type | Required, must be "Add" or "Remove" |
| Points Amount | Required, positive integer, minimum 1 |
| Reason | Required, minimum 10 characters, maximum 500 characters |

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No company selected | "Please select a company" | Highlight company list |
| No amount entered | "Please enter an amount" | Highlight field |
| Zero amount | "Amount must be at least 1 point" | Highlight field |
| Negative amount | "Amount must be a positive number" | Highlight field |
| No reason | "Please provide a reason for the adjustment" | Highlight field |
| Reason too short | "Reason must be at least 10 characters" | Highlight field |
| Insufficient balance (removal) | "Company only has X points. Cannot remove Y points." | Show warning |

**Success Criteria:**
- Admin can add or remove points from any company
- Reason is mandatory for every adjustment
- Points ledger entry created (immutable, append-only)
- Audit log records admin who made the change
- Company balance updated immediately

---

## Phase 5: SwapJoys Admin - Adjustment History

**Goal:** Admin views audit trail of all point adjustments made

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.1 | Admin clicks "Adjustment History" tab | Navigate to Adjustment History page |
| 5.2 | — | Load all admin point adjustments |
| 5.3 | — | Display adjustments in table (newest first) |
| 5.4 | Admin sees columns | Show: Date, Admin Name, Company, Type (Add/Remove), Amount, Reason, Balance After |
| 5.5 | Admin filters by company | Select company from dropdown |
| 5.6 | Admin filters by date range | Select start and end date |
| 5.7 | Admin filters by type | Select: All, Add, Remove |
| 5.8 | Admin views adjustment detail | Click row for full detail view |
| 5.9 | — | Display: Adjustment ID, Date/Time, Admin Name, Company, Type, Amount, Balance Before, Balance After, Reason |

**Success Criteria:**
- Complete audit trail of all adjustments
- All adjustments traceable to specific admin user
- Cannot edit or delete past adjustments (immutable)
- Filters work correctly

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | Points & Balance Dashboard | Sidebar "Points & Balance" | Click "View All" → Transaction History |
| 2 | Transaction History | "View All Transactions" link | Back → Dashboard |
| 3 | Transaction Detail | Click transaction row | Back → Transaction History |
| 4 | Admin - Point Adjustments | Admin sidebar "Point Adjustments" | Submit → Updated list |
| 5 | Admin - Adjustment History | Admin sidebar or tab | Click row → Detail |
| 6 | Admin - Adjustment Detail | Click adjustment row | Back → Adjustment History |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| Adjustment Type | Required, "Add" or "Remove" |
| Points Amount | Required, Positive integer, Min 1 |
| Reason | Required, Min 10 characters, Max 500 characters |
| Company Selection | Required, Must exist in system |
| Date Range Filter | Optional, Start date ≤ End date |

---

## Points Calculation

| Calculation | Formula |
|-------------|---------|
| Current Balance | Total Earned − Total Spent |
| Total Earned | Welcome Bonus + All Redemption Credits + Admin Additions |
| Total Spent | All Booking Deductions + Admin Removals |
| Balance After | Previous Balance + Points (for credit) or Previous Balance − Points (for debit) |

---

## Navigation Changes

### Company User (Owner/Manager) Navigation
- Dashboard
- Marketplace
- My Bookings
- **Points & Balance** ✅ (F8, F9)
- Employees
- Experiences
- Tax Reports
- Settings

### SwapJoys Admin Navigation
- Admin Dashboard
- Companies
- Experiences
- Usage Logs
- **Point Adjustments** ✅ (F10)
- Settings

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| View Points Dashboard | ✅ | ✅ | ❌ | ❌ |
| View Transaction History | ✅ | ✅ | ❌ | ❌ |
| View Balance on Dashboard | ✅ | ✅ | ✅ | ❌ |
| View Points on Experiences | ✅ | ✅ | ✅ | ❌ |
| Admin Adjust Points | ❌ | ❌ | ❌ | ✅ |
| Admin View Adjustment History | ❌ | ❌ | ❌ | ✅ |
| Admin View Company Balances | ❌ | ❌ | ❌ | ✅ |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 6 of 8
