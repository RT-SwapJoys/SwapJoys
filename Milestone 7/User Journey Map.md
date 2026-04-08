# SwapJoys Platform - User Journey Map
## Milestone 7: Admin Dashboard & Tax Module Part 1 (Features 11, 12, 15, 16, 17)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 7 of 8 |
| **Features** | SwapJoys Admin Dashboard (F11), Company & Employee Usage Logs (F12), Estimated Value Field (F15), Welfare Classification (F16), Usage Documentation (F17) |
| **Prepared by** | Rebing Tech |
| **Date** | April 2026 |
| **Status** | Ready for Client Approval |

---

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Company Dashboard | View company overview, stats, recent activity at a glance | Owner/Manager/Employee |
| Phase 2 | Admin Dashboard Overview | View key platform metrics and manage companies | SwapJoys Admin |
| Phase 3 | Company & Experience Management | View, inspect, and manage companies and experiences | SwapJoys Admin |
| Phase 4 | Transaction & Usage Logs | View all platform activity with filters and CSV export | SwapJoys Admin |
| Phase 5 | Estimated Value & Welfare Display | See NOK value and welfare tag on experiences and tickets | Owner/Manager/Employee |
| Phase 6 | Usage Documentation Logging | View employee usage logs with details for tax documentation | Owner/Manager |

---

## Phase 1: Company Dashboard (Owner/Manager/Employee)

**Goal:** Company users see an overview of their company's activity, stats, and quick actions on login

### Phase 1A: Owner/Manager Dashboard

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | User logs in or clicks "Dashboard" in sidebar | Navigate to Company Dashboard |
| 1.2 | — | Load company-specific data |
| 1.3 | — | Display Welcome message: "Welcome back, [Name]" with company name |
| 1.4 | — | Display stat cards: Points Balance, Total Employees, Active Experiences, Total Bookings |
| 1.5 | — | Display Points Activity chart (bar chart: earned vs spent, last 6 months) |
| 1.6 | — | Display Booking Status chart (doughnut: Used, Confirmed, Pending, Rejected) |
| 1.7 | — | Display Recent Bookings section (last 5 incoming + outgoing bookings with status badges) |
| 1.6 | — | Display Recent Redemptions section (last 5 redemptions with employee, experience, date) |
| 1.7 | — | Display Quick Actions: Create Experience, Add Employee, View Points, Redeem Ticket |
| 1.8 | User clicks a stat card | Navigate to relevant page (Points & Balance, Employees, etc.) |
| 1.9 | User clicks a booking entry | Navigate to booking detail |
| 1.10 | User clicks a quick action | Navigate to relevant page |

### Phase 1B: Employee Dashboard

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.11 | Employee logs in or clicks "Dashboard" in sidebar | Navigate to Employee Dashboard |
| 1.12 | — | Display Welcome message: "Welcome back, [Name]" |
| 1.13 | — | Display stat cards: Available Experiences, My Bookings, Experiences Used |
| 1.14 | — | Display My Experiences chart (bar chart: experiences used per month, last 6 months) |
| 1.15 | — | Display Experiences by Category chart (doughnut: Wellness, Dining, Fitness, etc.) |
| 1.16 | — | Display My Upcoming Bookings (confirmed tickets not yet used) |
| 1.15 | — | Display Recently Used Experiences (last 5 redeemed) |
| 1.16 | — | Display Quick Actions: Browse Experiences, View My Bookings |

**Success Criteria:**
- Dashboard loads with accurate data for the logged-in user
- Owner/Manager sees full company stats
- Employee sees only their personal stats
- Quick actions navigate to correct pages
- Recent activity shows latest entries
- Stat cards are clickable and navigate correctly

**Role-Based Dashboard Content:**

| Content | Owner | Manager | Employee |
|---------|:-----:|:-------:|:--------:|
| Points Balance card | Yes | Yes | - |
| Total Employees card | Yes | Yes | - |
| Active Experiences card | Yes | Yes | - |
| Total Bookings card | Yes | Yes | - |
| Available Experiences card | - | - | Yes |
| My Bookings card | - | - | Yes |
| Experiences Used card | - | - | Yes |
| Recent Bookings (company) | Yes | Yes | - |
| Recent Redemptions (company) | Yes | Yes | - |
| My Upcoming Bookings | - | - | Yes |
| Recently Used Experiences | - | - | Yes |
| Quick Action: Create Experience | Yes | Yes | - |
| Quick Action: Add Employee | Yes | Yes | - |
| Quick Action: View Points | Yes | Yes | - |
| Quick Action: Redeem Ticket | Yes | Yes | - |
| Quick Action: Browse Experiences | - | - | Yes |
| Quick Action: View My Bookings | - | - | Yes |

---

## Phase 2: Admin Dashboard Overview

**Goal:** SwapJoys platform admin views key metrics and overall platform health

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | Admin logs into SwapJoys Admin panel | Authenticate admin credentials, display Admin Dashboard |
| 1.2 | — | Load platform-wide metrics |
| 1.3 | — | Display Total Companies card (registered count) |
| 1.4 | — | Display Total Employees card (all employees across companies) |
| 1.5 | — | Display Total Experiences card (published count) |
| 1.6 | — | Display Total Redemptions card (completed redemptions) |
| 1.7 | — | Display Total Points in Circulation (sum of all company balances) |
| 1.8 | — | Display Platform Growth chart (line chart: companies + employees per month) |
| 1.9 | — | Display Monthly Redemptions chart (bar chart: redemption count per month) |
| 1.10 | — | Display Points by Company chart (doughnut: distribution across top companies) |
| 1.11 | — | Display Recent Activity feed (last 10 platform events) |
| 1.9 | Admin clicks on a metric card | Navigate to relevant detail page (Companies, Experiences, etc.) |
| 1.10 | Admin views sidebar navigation | Show admin menu: Dashboard, Companies, Experiences, Usage Logs, Point Adjustments, Settings |

**Success Criteria:**
- Dashboard loads with accurate real-time metrics
- All metric cards display correct counts
- Recent activity shows latest platform events
- Navigation to all admin sections works correctly

---

## Phase 3: Company & Experience Management

**Goal:** Admin views, inspects, and manages companies and experiences on the platform

### Phase 2A: Company Management

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | Admin clicks "Companies" in sidebar | Navigate to Company List page |
| 2.2 | — | Load all registered companies |
| 2.3 | — | Display company table: Name, Org Number, Status, Employees, Balance, Joined Date |
| 2.4 | Admin searches for a company | Filter list by company name or org number |
| 2.5 | Admin clicks on a company row | Navigate to Company Detail page |
| 2.6 | — | Display company info: Name, Org Number, Address, City, Contact, Email |
| 2.7 | — | Display company stats: Employee Count, Experience Count, Points Balance, Total Redemptions |
| 2.8 | — | Display employee list for this company |
| 2.9 | Admin clicks "Activate" or "Suspend" | Show confirmation dialog |
| 2.10 | Admin confirms status change | Update company status, show success message |

### Phase 2B: Experience Management

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.11 | Admin clicks "Experiences" in sidebar | Navigate to Experience List page |
| 2.12 | — | Load all platform experiences |
| 2.13 | — | Display experience table: Title, Company, Category, City, Points, NOK Value, Welfare Tag, Status |
| 2.14 | Admin searches experiences | Filter by title or company name |
| 2.15 | Admin filters by category | Filter dropdown: All, Dining, Wellness, Entertainment, etc. |
| 2.16 | Admin filters by city | Filter dropdown: All cities |
| 2.17 | Admin clicks on an experience row | Navigate to Experience Detail page |
| 2.18 | — | Display full experience info: Title, Description, Photo, Rules, Capacity, Points, NOK Value, Welfare Tag, Company, Status |

**Success Criteria:**
- All companies displayed with correct details
- Company search and filtering works
- Activate/Suspend company status works with confirmation
- All experiences displayed with NOK value and welfare tag visible
- Experience filters work individually and in combination

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No companies found | "No companies match your search" | Show clear search button |
| No experiences found | "No experiences match your filters" | Show clear filters button |

---

## Phase 4: Transaction & Usage Logs

**Goal:** Admin views all platform activity, filters logs, and exports data as CSV

### Phase 3A: Transaction Log

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | Admin clicks "Usage Logs" in sidebar | Navigate to Usage Logs page |
| 3.2 | — | Display tabs: Transaction Log, Redemption Log, Company Activity, Employee Activity |
| 3.3 | — | Default to Transaction Log tab |
| 3.4 | — | Load all platform transactions |
| 3.5 | — | Display table: Date, Type, Company (From), Company (To), Experience, Points, NOK Value |
| 3.6 | Admin filters by date range | Select start and end date |
| 3.7 | Admin filters by company | Select company from dropdown |
| 3.8 | Admin filters by type | Select: All, Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment |
| 3.9 | Admin clicks "Export CSV" | Generate and download CSV file with filtered data |

### Phase 3B: Redemption Log

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.10 | Admin clicks "Redemption Log" tab | Switch to Redemption Log view |
| 3.11 | — | Load all completed redemptions |
| 3.12 | — | Display table: Date, Employee, Experience, Host Company, Requesting Company, Points, NOK Value, Welfare Tag |
| 3.13 | Admin filters by date range | Filter redemptions by date |
| 3.14 | Admin filters by company | Filter by host or requesting company |
| 3.15 | Admin clicks "Export CSV" | Download redemption log as CSV |

### Phase 3C: Company Activity Log

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.16 | Admin clicks "Company Activity" tab | Switch to Company Activity view |
| 3.17 | Admin selects a company | Load activity for selected company |
| 3.18 | — | Display: Registrations, Bookings Made, Bookings Received, Redemptions, Point Changes |
| 3.19 | Admin filters by date range | Filter activity by date |
| 3.20 | Admin clicks "Export CSV" | Download company activity as CSV |

### Phase 3D: Employee Activity Log

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.21 | Admin clicks "Employee Activity" tab | Switch to Employee Activity view |
| 3.22 | Admin selects a company, then an employee | Load activity for selected employee |
| 3.23 | — | Display: Experiences Used, Dates, NOK Values, Welfare Tags, Total Value |
| 3.24 | Admin filters by date range | Filter by date |
| 3.25 | Admin clicks "Export CSV" | Download employee activity as CSV |

**Success Criteria:**
- All log tabs display correct data
- Filters work individually and in combination across all tabs
- CSV export generates correct file with filtered data
- Pagination works for large datasets (20 per page)
- NOK values and welfare tags visible in all relevant logs

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No logs found | "No records found for the selected filters" | Show clear filters button |
| CSV empty | "No data to export" | Disable export button when no data |

---

## Phase 5: Estimated Value & Welfare Display

**Goal:** Users see NOK estimated value and welfare classification on experiences and tickets

### Phase 4A: Estimated Value Field (F15)

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | User views experience detail page | Display "Estimated Value (NOK)" field prominently |
| 4.2 | — | Show value format: "NOK 1,500" |
| 4.3 | User views experience card in marketplace | Display NOK value on card alongside points |
| 4.4 | User receives a ticket after booking approval | Ticket stores the NOK value at time of booking |
| 4.5 | User views transaction history | NOK value displayed alongside points in transaction records |
| 4.6 | Admin views experience in admin panel | NOK value visible in experience detail and lists |

### Phase 4B: Welfare Classification (F16)

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.7 | User views experience detail page | Display welfare badge: "Welfare Benefit" (green) or "Not Welfare" (gray) |
| 4.8 | User views experience card in marketplace | Show welfare badge icon on card |
| 4.9 | User receives a ticket after booking approval | Ticket stores the welfare classification status |
| 4.10 | User views usage reports | Welfare tag included in all report data |
| 4.11 | Admin views experience in admin panel | Welfare status visible in experience lists and details |

**Success Criteria:**
- NOK value displayed on experience detail, cards, tickets, and transactions
- Welfare badge displayed on experience detail, cards, and tickets
- Values stored immutably with tickets at time of booking
- Welfare tag included in all reports and exports

---

## Phase 6: Usage Documentation Logging

**Goal:** Company owners/managers view employee usage logs for tax documentation purposes

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.1 | Owner/Manager clicks "Tax Reports" in sidebar | Navigate to Usage Documentation page |
| 5.2 | — | Load employee usage logs for the company |
| 5.3 | — | Display table: Date, Employee Name, Experience Name, Host Company, NOK Value, Welfare Tag |
| 5.4 | — | Auto-log created on every ticket redemption |
| 5.5 | User filters by employee | Select employee from dropdown |
| 5.6 | User filters by date range | Select start and end date |
| 5.7 | User filters by welfare status | Filter: All, Welfare Only, Non-Welfare Only |
| 5.8 | User views usage summary | Display total NOK value per employee at top |
| 5.9 | User clicks on a log entry | Show full detail: Employee, Experience, Date, NOK Value, Company, Welfare Tag, Ticket Reference |
| 5.10 | — | Display running total of welfare benefits per employee |

**Success Criteria:**
- Usage log automatically created on every redemption
- Log contains: Employee name, Experience name, Date, Estimated value, Company, Welfare tag
- Filters work correctly for employee, date range, and welfare status
- Running totals calculated per employee
- Data is accurate and matches actual redemptions

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No usage logs | "No usage records found" | Show message with explanation |
| No filter results | "No records match your filters" | Show clear filters button |

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | Company Dashboard (Owner/Manager) | Login / Sidebar "Dashboard" | Click stat/action → Relevant page |
| 2 | Company Dashboard (Employee) | Login / Sidebar "Dashboard" | Click action → Relevant page |
| 3 | Admin Dashboard Overview | Admin login | Click metric → Detail pages |
| 4 | Admin - Company List | Sidebar "Companies" | Click row → Company Detail |
| 5 | Admin - Company Detail | Click company row | Back → Company List |
| 6 | Admin - Experience List | Sidebar "Experiences" | Click row → Experience Detail |
| 7 | Admin - Experience Detail | Click experience row | Back → Experience List |
| 8 | Admin - Transaction Log | Sidebar "Usage Logs" | Export CSV / Switch tabs |
| 9 | Admin - Redemption Log | "Redemption Log" tab | Export CSV / Switch tabs |
| 10 | Admin - Company Activity | "Company Activity" tab | Export CSV / Switch tabs |
| 11 | Admin - Employee Activity | "Employee Activity" tab | Export CSV / Switch tabs |
| 12 | Experience Detail (NOK + Welfare) | Marketplace click | Back → Marketplace |
| 13 | Company - Usage Documentation | Sidebar "Tax Reports" | Filter / View detail |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| Admin Login | Required email + password, admin role verification |
| Company Search | Optional, filters as user types |
| Experience Filters | Optional, category + city work together |
| Log Date Range | Optional, Start date <= End date |
| Log Company Filter | Optional, select from registered companies |
| Log Type Filter | Optional, select from transaction types |
| CSV Export | Only exports currently filtered data |

---

## Navigation Changes

### Company User (Owner/Manager) Navigation
- Dashboard
- Experiences (Marketplace)
- My Bookings
- Points & Balance
- Employees
- My Experiences
- **Tax Reports** (F17 - Usage Documentation)
- Redeem Ticket
- Settings

### SwapJoys Admin Navigation
- **Admin Dashboard** (F11)
- **Companies** (F11)
- **Experiences** (F11)
- **Usage Logs** (F12)
- Point Adjustments
- Settings

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| View Company Dashboard | Yes | Yes | Yes | - |
| View Admin Dashboard | - | - | - | Yes |
| View/Manage Companies | - | - | - | Yes |
| View/Manage Experiences (Admin) | - | - | - | Yes |
| View Transaction Logs | - | - | - | Yes |
| View Redemption Logs | - | - | - | Yes |
| View Company Activity Logs | - | - | - | Yes |
| View Employee Activity Logs | - | - | - | Yes |
| Export Logs CSV | - | - | - | Yes |
| View NOK Value on Experiences | Yes | Yes | Yes | Yes |
| View Welfare Tag on Experiences | Yes | Yes | Yes | Yes |
| View Usage Documentation (Tax) | Yes | Yes | - | - |
| Filter Usage Logs by Employee | Yes | Yes | - | - |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 7 of 8
