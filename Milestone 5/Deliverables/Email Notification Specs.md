# SwapJoys Platform - Email Notification Specifications
## Milestone 5: Booking & QR Verification (Features 6, 7, 13)

| | |
|---|---|
| **Project** | SwapJoys Platform MVP |
| **Milestone** | 5 of 8 |
| **Prepared by** | Rebing Tech |
| **Date** | March 2026 |
| **Status** | Ready for Client Approval |

---

## Email Overview

Milestone 5 introduces **4 transactional emails** triggered by booking and redemption events.

| # | Email | Trigger | Recipient | Priority |
|---|-------|---------|-----------|----------|
| 1 | New Request Received | Requesting company submits booking request | Host company Owner + Manager(s) | High |
| 2 | Request Approved (Ticket Created) | Host approves a request | Requesting company Owner + Manager(s) + Assigned employee | High |
| 3 | Request Rejected | Host rejects a request | Requesting company Owner + Manager(s) | Medium |
| 4 | Ticket Redeemed | Host scans QR / enters code | Requesting company Owner + Manager(s) + Assigned employee | Medium |

---

## Email 1: New Request Received

**Trigger:** Requesting company submits a booking request  
**Recipient:** Host company Owner and all Manager(s)  
**Subject Line:** `New experience request from {requesting_company_name}`

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

   [SwapJoys Logo]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Hi {host_owner_name},

You have a new request for your experience.

EXPERIENCE
{experience_title}

REQUESTING COMPANY
{requesting_company_name}

ASSIGNED EMPLOYEE
{employee_name}

PREFERRED DATE
{preferred_date}

MESSAGE
"{message_text}"
(or: "No message included." if empty)

            [ Review Request ]

Log in to SwapJoys to approve or decline
this request.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
© 2026 SwapJoys. All rights reserved.
```

---

## Email 2: Request Approved (Ticket Created)

**Trigger:** Host company approves the booking request  
**Recipient:** Requesting company Owner, Manager(s), and assigned employee  
**Subject Line:** `Your request for "{experience_title}" has been approved!`

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

   [SwapJoys Logo]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Great news! Your experience request has
been approved.

EXPERIENCE
{experience_title}

HOST COMPANY
{host_company_name}

ASSIGNED EMPLOYEE
{employee_name}

PREFERRED DATE
{preferred_date}

POINTS DEDUCTED
{point_cost} points from your balance

YOUR TICKET
A ticket has been created. The assigned
employee can view the QR code by logging
into SwapJoys.

Backup Code: {backup_code}

            [ View Ticket ]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
© 2026 SwapJoys. All rights reserved.
```

---

## Email 3: Request Rejected

**Trigger:** Host company rejects the booking request  
**Recipient:** Requesting company Owner and Manager(s)  
**Subject Line:** `Update on your request for "{experience_title}"`

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

   [SwapJoys Logo]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Hi {requesting_owner_name},

Unfortunately, your experience request
was not approved.

EXPERIENCE
{experience_title}

HOST COMPANY
{host_company_name}

REASON
"{rejection_reason}"

No points have been deducted from your
balance.

You can browse other experiences on the
marketplace or submit a new request.

         [ Browse Marketplace ]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
© 2026 SwapJoys. All rights reserved.
```

---

## Email 4: Ticket Redeemed

**Trigger:** Host scans QR code or enters backup code, confirms redemption  
**Recipient:** Requesting company Owner, Manager(s), and assigned employee  
**Subject Line:** `Experience redeemed: "{experience_title}"`

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

   [SwapJoys Logo]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

An experience has been successfully
redeemed.

EXPERIENCE
{experience_title}

HOST COMPANY
{host_company_name}

EMPLOYEE
{employee_name}

REDEEMED ON
{redemption_date} at {redemption_time}

POINTS
{point_cost} points

ESTIMATED VALUE
{estimated_value_nok} NOK

WELFARE BENEFIT
{welfare_tag} (Yes/No)

This redemption has been logged for your
tax documentation records.

         [ View Bookings ]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
© 2026 SwapJoys. All rights reserved.
```

---

## Email Template Variables

| Variable | Source | Example |
|----------|--------|---------|
| `{host_owner_name}` | Host company owner's name | "Erik Johansen" |
| `{requesting_company_name}` | Company that submitted request | "TechCorp AS" |
| `{requesting_owner_name}` | Requesting company owner's name | "Selim Tesfamariam" |
| `{host_company_name}` | Company hosting the experience | "Nordic Wellness AS" |
| `{experience_title}` | Title of the experience | "Spa Day Package" |
| `{employee_name}` | Assigned employee's full name | "Kari Nordmann" |
| `{preferred_date}` | Selected date, formatted | "March 15, 2026" |
| `{message_text}` | Optional message from requester | "Looking forward to this!" |
| `{rejection_reason}` | Reason provided by host | "Fully booked for March" |
| `{point_cost}` | Points for the experience | "50" |
| `{backup_code}` | 6-char alphanumeric ticket code | "A7K9M2" |
| `{redemption_date}` | Date of redemption | "March 15, 2026" |
| `{redemption_time}` | Time of redemption | "14:30" |
| `{estimated_value_nok}` | Tax value in NOK | "500" |
| `{welfare_tag}` | Welfare benefit classification | "Yes" or "No" |

---

## Email Design Specifications

| Property | Value |
|----------|-------|
| From Name | SwapJoys |
| From Email | noreply@swapjoys.com |
| Template Style | Consistent with M2/M3 emails (logo header, clean layout) |
| Primary Button Color | `#244899` (SwapJoys blue) |
| Button Style | Rounded corners, centered, 600px max-width |
| Footer | "© 2026 SwapJoys. All rights reserved." |
| Responsive | Mobile-friendly, single column layout |

---

## Email Sending Rules

| Rule | Detail |
|------|--------|
| Delivery | Immediate on trigger event |
| Duplicates | One email per recipient per event (no duplicates) |
| Owner is also Manager | Send only one email (Owner takes priority) |
| Assigned employee | Receives approval and redemption emails only |
| Failed sends | Log error, do not block the action |
| Unsubscribe | Not applicable for transactional emails |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 5 of 8
