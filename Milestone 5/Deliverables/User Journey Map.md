# SwapJoys Platform - User Journey Map
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

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Request Experience | Submit a booking request for an experience | Requesting Company (Owner/Manager) |
| Phase 2 | Manage Incoming Requests | Review, approve, or reject requests | Host Company (Owner/Manager) |
| Phase 3 | My Bookings | View all outgoing bookings and their status | Requesting Company (All Roles) |
| Phase 4 | Ticket & QR Code | View ticket, display QR to host | Assigned Employee |
| Phase 5 | QR Scanner & Redemption | Scan QR or enter code to redeem ticket | Host Company (Owner/Manager) |
| Phase 6 | Status Tracking | Track experience status across all views | All Roles |

---

## Phase 1: Request Experience

**Goal:** Owner/Manager submits a booking request from the marketplace

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | User views Experience Detail in marketplace | Display experience with "Request Experience" button |
| 1.2 | Clicks "Request Experience" button | Open Request modal/form |
| 1.3 | — | Check company point balance ≥ experience point cost |
| 1.4 | — | If insufficient points: show warning "Insufficient balance (X points). This experience costs Y points." and disable submit |
| 1.5 | Selects employee from dropdown | Show company employees (active only) |
| 1.6 | Selects preferred date | Date picker (must be today or future) |
| 1.7 | Enters message to host (optional) | Max 500 characters |
| 1.8 | Clicks "Submit Request" | Validate all fields |
| 1.9 | — | Create booking record (status: Pending) |
| 1.10 | — | Send email notification to host company Owner/Manager(s) |
| 1.11 | — | Show success message: "Request submitted! The host company will review your request." |
| 1.12 | — | Redirect to My Bookings page |

**Success Criteria:**
- Booking record created with status "Pending"
- Points NOT deducted yet (only on approval)
- Host company notified via email
- Booking appears in requesting company's "My Bookings" list
- Booking appears in host company's "Incoming Requests" list

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Insufficient points | "Your company needs X more points to request this experience" | Disable submit, show balance |
| No employees available | "No active employees found. Please add employees first." | Link to Employees page |
| No date selected | "Please select a preferred date" | Highlight field |
| Experience at capacity | "This experience has reached its maximum bookings" | Disable request button |
| Already requested | "Your company already has a pending request for this experience" | Show existing request link |

---

## Phase 2: Manage Incoming Requests

**Goal:** Host company Owner/Manager reviews and acts on incoming booking requests

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | User clicks "My Bookings" in sidebar | Navigate to Bookings page |
| 2.2 | Clicks "Incoming Requests" tab | Show requests from other companies |
| 2.3 | — | Display request cards/list with: Company name, Employee name, Experience name, Preferred date, Message, Status badge, Date submitted |
| 2.4 | User sees stats cards | Show: Total Incoming, Pending, Approved, Rejected counts |
| 2.5 | User clicks on a request | Open Request Detail modal/view |
| 2.6 | Reviews full request details | Display all request information |

### Approve Flow

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.A1 | Clicks "Approve" button | Show confirmation: "Approve this request? X points will be deducted from the requesting company." |
| 2.A2 | Confirms approval | Update booking status to "Confirmed" |
| 2.A3 | — | Deduct points from requesting company balance |
| 2.A4 | — | Generate QR code (unique per ticket) |
| 2.A5 | — | Generate 6-character alphanumeric backup code |
| 2.A6 | — | Create ticket record (status: Confirmed) |
| 2.A7 | — | Create transaction log entry (points deduction) |
| 2.A8 | — | Send approval email to requesting company with ticket details |
| 2.A9 | — | Show success message: "Request approved. Ticket created." |

### Reject Flow

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.R1 | Clicks "Reject" button | Open rejection modal |
| 2.R2 | Enters rejection reason (required) | Min 10 characters |
| 2.R3 | Clicks "Confirm Rejection" | Update booking status to "Rejected" |
| 2.R4 | — | NO points deducted (request was pending) |
| 2.R5 | — | Send rejection email to requesting company with reason |
| 2.R6 | — | Show confirmation message: "Request rejected." |

**Success Criteria:**
- All incoming requests visible with status
- Approve creates ticket with QR + backup code
- Points deducted only on approval
- Reject requires reason
- Both actions trigger email notifications

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Requesting company deleted balance mid-process | "Unable to process. Please try again." | Refresh request |
| Rejection reason too short | "Please provide a reason (min 10 characters)" | Highlight field |

---

## Phase 3: My Bookings (Outgoing)

**Goal:** Requesting company views all their outgoing booking requests and tickets

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | User clicks "My Bookings" in sidebar | Navigate to Bookings page |
| 3.2 | "Outgoing Bookings" tab is active by default | Show all bookings made by the company |
| 3.3 | — | Display booking cards with: Experience name, Host company, Assigned employee, Status badge, Preferred date, Points cost |
| 3.4 | User sees stats cards | Show: Total, Pending, Confirmed, Used, Rejected counts |
| 3.5 | User filters by status | Dropdown: All, Pending, Confirmed, Used, Rejected |
| 3.6 | User clicks a Confirmed booking | Navigate to Ticket View |
| 3.7 | User clicks a Pending booking | Show request details (waiting for host response) |
| 3.8 | User clicks a Rejected booking | Show rejection reason from host |
| 3.9 | User clicks a Used booking | Show redemption details (date, time) |

**Success Criteria:**
- All outgoing bookings listed with correct status
- Confirmed bookings link to ticket/QR view
- Rejected bookings show reason
- Status filters work correctly

---

## Phase 4: Ticket & QR Code Display

**Goal:** Assigned employee views their ticket and displays QR code to host for redemption

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | Employee clicks "My Bookings" or "My Tickets" | Navigate to tickets list |
| 4.2 | Clicks on a confirmed ticket | Navigate to Ticket View page |
| 4.3 | — | Display ticket information: Experience name, Host company, Assigned employee name, Preferred date, Status: Confirmed, Point cost |
| 4.4 | — | Display QR code (large, scannable) |
| 4.5 | — | Display 6-character backup code below QR |
| 4.6 | User clicks "Show to Host" button | Enter full-screen QR mode |
| 4.7 | — | Display QR code maximized, high contrast, dark background |
| 4.8 | — | Show backup code prominently below QR |
| 4.9 | — | Show "Tap anywhere to exit" instruction |
| 4.10 | User taps screen | Exit full-screen mode |

**Ticket Information Displayed:**

| Field | Example |
|-------|---------|
| Experience Title | "Spa Day Package" |
| Host Company | Nordic Wellness AS |
| Employee | Kari Nordmann |
| Preferred Date | March 15, 2026 |
| Status | Confirmed ✅ |
| Points | 50 |
| QR Code | [Generated QR image] |
| Backup Code | `A7K9M2` |

**Success Criteria:**
- QR code is unique and scannable
- Backup code is clearly visible
- Full-screen mode works on mobile
- Only confirmed (unused) tickets show QR
- Used tickets show "Redeemed" status instead of QR

---

## Phase 5: QR Scanner & Redemption

**Goal:** Host company scans QR code or enters backup code to redeem a ticket

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.1 | Host Owner/Manager navigates to "Scan Ticket" | Open Scanner page |
| 5.2 | — | Request camera permission |
| 5.3 | (If camera denied) User sees manual entry option | Show "Enter Code Manually" input field |
| 5.4 | Points camera at employee's QR code | Scan and decode QR code |
| 5.5 | — | Validate: code exists, not expired, not already used, belongs to host's experience |
| 5.6 | — | Display ticket summary for confirmation: Employee name, Experience name, Requesting company, Point value |
| 5.7 | Host clicks "Confirm Redemption" | Mark ticket as "Used" |
| 5.8 | — | Credit points to host company balance |
| 5.9 | — | Create transaction log entry (points credit to host) |
| 5.10 | — | Create usage documentation record (for tax: employee, experience, date, value, company, welfare tag) |
| 5.11 | — | Display success screen: "Experience redeemed! +X points credited to your balance." |
| 5.12 | — | Send redemption confirmation email to requesting company |

### Manual Code Entry (Backup)

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.M1 | User clicks "Enter Code Manually" | Show text input field |
| 5.M2 | Enters 6-character code | Validate format (alphanumeric, 6 chars) |
| 5.M3 | Clicks "Verify Code" | Same validation as QR scan (step 5.5) |
| 5.M4 | — | Continue from step 5.6 (show ticket summary) |

**Success Criteria:**
- QR scanning works with device camera
- Manual backup code entry works as fallback
- Points credited to host company on redemption
- Ticket marked as "Used" — cannot be redeemed again
- Transaction logged in immutable ledger
- Usage documentation created for tax module

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Camera permission denied | "Camera access required for QR scanning" | Show manual entry option |
| Invalid QR code | "Invalid ticket. This QR code is not recognized." | Show retry option |
| Ticket already used | "This ticket has already been redeemed on [date]." | Show details |
| Ticket expired | "This ticket has expired." | Show details |
| Wrong host | "This ticket is not for your experience." | Show error |
| Invalid manual code | "Code not found. Please check and try again." | Clear input |

---

## Phase 6: Status Tracking (Feature 13)

**Goal:** All users can see accurate status of bookings/tickets across the platform

### Status Definitions

| Status | When | Badge Color | Icon |
|--------|------|-------------|------|
| **Pending** | Request submitted, awaiting host response | Orange/Yellow | ⏳ Clock |
| **Confirmed** | Host approved, ticket created, QR generated | Blue | ✅ Check |
| **Used** | QR scanned or code entered, experience redeemed | Green | ✔️ Double check |
| **Rejected** | Host declined the request | Red | ✕ Cross |

### Status Visibility Across Views

| View | Statuses Shown | Actor |
|------|----------------|-------|
| My Bookings (Outgoing) | Pending, Confirmed, Used, Rejected | Requesting Company |
| Incoming Requests | Pending, Confirmed, Used, Rejected | Host Company |
| My Tickets | Confirmed, Used | Assigned Employee |
| SwapJoys Admin Dashboard | All statuses | SwapJoys Admin |

### Status Transitions

| From | To | Trigger | Actor |
|------|-----|---------|-------|
| — | Pending | Request submitted | Requesting Company |
| Pending | Confirmed | Host approves | Host Company |
| Pending | Rejected | Host rejects | Host Company |
| Confirmed | Used | QR scanned / code entered | Host Company |

**Rules:**
- Status can only move forward, never backward
- Rejected bookings cannot be re-opened (must create new request)
- Used tickets cannot be reverted
- Pending requests can only become Confirmed or Rejected

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | Request Experience Modal | "Request" button on Experience Detail | Submit → My Bookings |
| 2 | My Bookings (Outgoing tab) | Sidebar "My Bookings" | Click booking → Detail |
| 3 | My Bookings (Incoming tab) | Sidebar "My Bookings" > Incoming | Click request → Detail |
| 4 | Request Detail (Incoming) | Click request in Incoming list | Approve/Reject |
| 5 | Rejection Reason Modal | "Reject" button | Submit → Incoming list |
| 6 | Booking Detail (Outgoing) | Click booking in Outgoing list | Back → My Bookings |
| 7 | Ticket View | Click confirmed booking | Show QR / Full-screen |
| 8 | QR Full-Screen | "Show to Host" button | Tap → exit |
| 9 | Scanner Page | "Scan Ticket" nav item or button | Scan → Confirmation |
| 10 | Manual Code Entry | "Enter Code Manually" on scanner | Verify → Confirmation |
| 11 | Redemption Confirmation | After successful scan/code | Done → Scanner |
| 12 | Rejected Booking Detail | Click rejected booking | Back → My Bookings |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| Employee Selection | Required, Must be active employee in company |
| Preferred Date | Required, Must be today or future date |
| Message to Host | Optional, Max 500 characters |
| Rejection Reason | Required, Min 10 characters, Max 500 characters |
| Backup Code (manual entry) | Required, Exactly 6 alphanumeric characters |

---

## Points Flow

| Event | Requesting Company | Host Company |
|-------|-------------------|--------------|
| Request Submitted | No change (points reserved/checked) | No change |
| Request Approved | −X points (deducted) | No change |
| Request Rejected | No change | No change |
| Ticket Redeemed | No change | +X points (credited) |

**Important:** Points are deducted from the requesting company when the host **approves** the request, NOT when the ticket is redeemed. The host receives points when the ticket is **redeemed** (QR scanned). This creates a two-step settlement: deduct on approval, credit on redemption.

---

## QR Code Specifications

| Property | Value |
|----------|-------|
| Content | Unique ticket UUID |
| Format | QR Code (Version auto-detected based on data) |
| Error Correction | Level M (15% recovery) |
| Minimum Size | 200×200 px (display), scalable |
| Full-Screen Size | Max device width, centered |
| Background | White with dark modules |
| Backup Code | 6 alphanumeric characters (uppercase + digits), e.g. `A7K9M2` |
| Code Uniqueness | Globally unique, never reused |

---

## Role-Based Access

| Action | Owner | Manager | Employee |
|--------|:-----:|:-------:|:--------:|
| Request Experience | ✅ | ✅ | ❌ |
| View Outgoing Bookings | ✅ | ✅ | ✅ (own only) |
| Approve/Reject Incoming | ✅ | ✅ | ❌ |
| View Ticket (QR) | ✅ | ✅ | ✅ (own only) |
| Full-Screen QR Display | ✅ | ✅ | ✅ (own only) |
| Scan QR / Enter Code | ✅ | ✅ | ❌ |
| View Status in Lists | ✅ | ✅ | ✅ (own only) |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 5 of 8
