# SwapJoys Platform - User Journey Map
## Milestone 3: Employee Onboarding & Roles (Features 2, 3)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 3 of 8 |
| **Features** | Employee Onboarding (F2), Role Assignment (F3) |
| **Prepared by** | Rebing Tech |
| **Date** | February 2026 |
| **Status** | Ready for Client Approval |

---

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Employee List | View all company employees | Owner/Manager |
| Phase 2 | Add Employee | Add new employee to company | Owner/Manager |
| Phase 3 | Employee Invitation | Accept invite and activate account | Invited Employee |
| Phase 4 | Role Management | Assign and manage employee roles | Owner/Manager |
| Phase 5 | Employee Profile | View and edit employee details | Owner/Manager |

---

## Phase 1: Employee List

**Goal:** Owner/Manager views all employees in their company

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | User clicks "Employees" in sidebar | Navigate to Employee List page |
| 1.2 | — | Load all employees for company |
| 1.3 | — | Display employee table with columns: Name, Email, Role, Status, Actions |
| 1.4 | User sees employee count | Display total: "18 Employees" |
| 1.5 | User views status badges | Show Active (green), Pending (orange), Inactive (gray) |
| 1.6 | User views role badges | Show Owner (purple), Manager (blue), Employee (gray) |
| 1.7 | User uses search box | Filter employees by name or email |
| 1.8 | User filters by role | Show dropdown: All, Owner, Manager, Employee |
| 1.9 | User filters by status | Show dropdown: All, Active, Pending, Inactive |
| 1.10 | User clicks "Add Employee" button | Navigate to Add Employee form |

**Success Criteria:**
- All company employees displayed
- Search and filters working
- Status and role badges visible
- Pagination for large lists (>10 employees)

---

## Phase 2: Add Employee

**Goal:** Owner/Manager adds a new employee to the company

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | User clicks "Add Employee" | Display Add Employee form/modal |
| 2.2 | Enters employee name | Validate min 2 characters |
| 2.3 | Enters employee email | Validate email format |
| 2.4 | Enters phone number (optional) | Validate Norwegian format |
| 2.5 | Selects role from dropdown | Show: Manager, Employee (Owner cannot be assigned) |
| 2.6 | — | Display role permissions info |
| 2.7 | Clicks "Send Invitation" | Validate all fields |
| 2.8 | — | Check email not already in company |
| 2.9 | — | Create employee record (status: pending) |
| 2.10 | — | Generate invitation token (7 days expiry) |
| 2.11 | — | Send invitation email |
| 2.12 | — | Show success message |
| 2.13 | — | Redirect to Employee List |
| 2.14 | — | New employee shows with "Pending" badge |

**Success Criteria:**
- Employee record created
- Invitation email sent
- Employee appears in list with Pending status

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Email exists in company | "Employee with this email already exists" | Highlight field |
| Email exists (other company) | "This email is registered with another company" | Show error |
| Invalid email | "Please enter a valid email address" | Highlight field |
| Name too short | "Name must be at least 2 characters" | Highlight field |

---

## Phase 3: Employee Invitation (Employee's Perspective)

**Goal:** Invited employee accepts invitation and activates account

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | Employee receives invitation email | Email contains company name, inviter name |
| 3.2 | Opens email inbox | — |
| 3.3 | Opens email from SwapJoys | — |
| 3.4 | Clicks "Accept Invitation" button | Validate invitation token |
| 3.5 | — | Check token not expired (7 days) |
| 3.6 | — | Display Account Activation page |
| 3.7 | Sees welcome message | "You've been invited to join [Company Name]" |
| 3.8 | Sees their assigned role | Display role with description |
| 3.9 | Enters new password | Validate password strength |
| 3.10 | Enters confirm password | Verify passwords match |
| 3.11 | Clicks "Activate Account" | Validate all fields |
| 3.12 | — | Update user password |
| 3.13 | — | Set status to "Active" |
| 3.14 | — | Delete invitation token |
| 3.15 | — | Display success message |
| 3.16 | — | Redirect to Login page |
| 3.17 | Employee logs in | Access dashboard based on role |

**Alternative Flow - Resend Invitation:**

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.A1 | Owner/Manager views pending employee | Show "Resend Invitation" button |
| 3.A2 | Clicks "Resend Invitation" | Generate new token |
| 3.A3 | — | Invalidate old token |
| 3.A4 | — | Send new invitation email |
| 3.A5 | — | Show confirmation message |

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Token expired | "Invitation has expired" | Show "Contact your company admin" |
| Token invalid | "Invalid invitation link" | Show error message |
| Already activated | "Account already activated" | Redirect to login |
| Weak password | "Password requirements not met" | Show requirements |

---

## Phase 4: Role Management

**Goal:** Owner/Manager assigns or changes employee roles

### Role Definitions

| Role | Slug | Access Level |
|------|------|--------------|
| **Owner** | `owner` | Full access: billing, settings, all features, can manage all roles |
| **Manager** | `manager` | Manage employees, experiences, approve bookings, view reports |
| **Employee** | `employee` | View marketplace, use tickets, view own bookings only |

### Permission Matrix

| Feature | Owner | Manager | Employee |
|---------|:-----:|:-------:|:--------:|
| View Dashboard | ✅ | ✅ | ✅ |
| View Marketplace | ✅ | ✅ | ✅ |
| Use Tickets | ✅ | ✅ | ✅ |
| View Own Bookings | ✅ | ✅ | ✅ |
| Create Experiences | ✅ | ✅ | ❌ |
| Approve Bookings | ✅ | ✅ | ❌ |
| Add/Edit Employees | ✅ | ✅ | ❌ |
| Change Employee Roles | ✅ | ❌ | ❌ |
| View All Transactions | ✅ | ✅ | ❌ |
| Tax Reports | ✅ | ❌ | ❌ |
| Subscription Management | ✅ | ❌ | ❌ |
| Company Settings | ✅ | ❌ | ❌ |

### Role Assignment Flow

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | Owner views employee details | Display current role |
| 4.2 | Clicks "Change Role" or role dropdown | Show available roles |
| 4.3 | Selects new role | Highlight selection |
| 4.4 | — | Show role permissions preview |
| 4.5 | Clicks "Save" or "Update" | Validate role change allowed |
| 4.6 | — | Update employee role in database |
| 4.7 | — | Show success message |
| 4.8 | — | Employee sees updated navigation on next login |

**Role Change Rules:**
- Only Owner can change roles
- Cannot demote the last Owner (must have at least 1 Owner)
- Manager can add employees but cannot change roles
- Cannot promote to Owner (Owner role is special)

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Last Owner | "Cannot change role. Company must have at least one Owner" | Disable action |
| No permission | "Only Owners can change employee roles" | Hide option for Managers |
| Self-demotion (last owner) | "Cannot demote yourself as the only Owner" | Show warning |

---

## Phase 5: Employee Profile Management

**Goal:** Owner/Manager views and edits employee details

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.1 | User clicks employee name/row in list | Navigate to Employee Detail page |
| 5.2 | — | Load employee data |
| 5.3 | Views employee information | Display: Name, Email, Phone, Role, Status, Join Date |
| 5.4 | Clicks "Edit" button | Enable edit mode |
| 5.5 | Edits employee name | Validate min 2 characters |
| 5.6 | Edits phone number | Validate format |
| 5.7 | (Owner only) Changes role | See Phase 4 |
| 5.8 | Clicks "Save Changes" | Validate all fields |
| 5.9 | — | Update employee in database |
| 5.10 | — | Show success message |

### Deactivate/Activate Employee

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.D1 | User clicks "Deactivate" on active employee | Show confirmation modal |
| 5.D2 | Confirms deactivation | Set status to "Inactive" |
| 5.D3 | — | Employee cannot login |
| 5.D4 | — | Show in list with gray "Inactive" badge |
| 5.D5 | User clicks "Activate" on inactive employee | Set status to "Active" |
| 5.D6 | — | Employee can login again |

**Cannot Deactivate:**
- The last Owner
- Your own account

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | Employee List | Sidebar "Employees" | Click employee or Add |
| 2 | Add Employee Modal | "Add Employee" button | Submit → List |
| 3 | Invitation Email | Sent after add | Click link → Activate |
| 4 | Account Activation | Email link click | Submit → Login |
| 5 | Activation Success | After activation | Button → Login |
| 6 | Employee Detail | Click employee in list | Save → List |
| 7 | Edit Employee | "Edit" button | Save → Detail |
| 8 | Role Selector | In employee detail | Save → Updated |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| Employee Name | Required, Min 2 characters, Max 100 characters |
| Employee Email | Required, Valid email format, Unique within company |
| Phone Number | Optional, Valid format (+47 XXX XX XXX) |
| Role | Required, Must be "manager" or "employee" |
| Password (Activation) | Required, Min 8 chars, 1 uppercase, 1 number |
| Confirm Password | Required, Must match password |

---

## Token Expiry

| Token Type | Expiry Time |
|------------|-------------|
| Employee Invitation | 7 days |
| JWT Session | 60 minutes (configurable) |

---

## Navigation Changes by Role

### Owner Navigation
- Dashboard
- Marketplace
- My Bookings
- Points & Balance
- **Employees** ✅
- Experiences
- Tax Reports
- Settings (Company + Subscription)

### Manager Navigation
- Dashboard
- Marketplace
- My Bookings
- Points & Balance
- **Employees** ✅
- Experiences
- Settings (Personal only)

### Employee Navigation
- Dashboard
- Marketplace
- My Bookings
- My Tickets
- Settings (Personal only)

---

## Email Template: Employee Invitation

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

   [SwapJoys Logo]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Hi {employee_name},

You've been invited to join {company_name} on SwapJoys - 
an employee experience exchange platform.

{inviter_name} has added you as a {role}.

        [Accept Invitation]

This link will expire in 7 days.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
© 2026 SwapJoys. All rights reserved.
```

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 3 of 8
