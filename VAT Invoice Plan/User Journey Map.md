# SwapJoys Platform - User Journey Map
## VAT / Invoicing Module (Features 7, 8, 14, 15, 16, 17, 18, 19, 20, 21)

| | |
|---|---|
| **Project** | SwapJoys Platform |
| **Module** | VAT / Invoicing |
| **Features** | Company VAT Number (F7), Invoice Email (F8), Register Sale (F14), Use Points (F15), PDF Invoice Generator (F16), Automatic Invoice Email (F17), Invoice Archive (F18), Swap Ledger with VAT (F19), Accounting Export (F20), Invoice Routing Logic (F21) |
| **Prepared by** | Rebing Tech |
| **Date** | April 2026 |
| **Status** | Ready for Client Review |

---

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Company Profile > VAT Settings | Set up company VAT/MVA number and invoice email | Owner |
| Phase 2 | Register Sale Form | Register a sale to another company with VAT breakdown | Owner/Manager (Seller) |
| Phase 3 | Use Points Form | Use points toward an experience or custom amount | Owner/Manager |
| Phase 4 | Invoice PDF & Email | System generates Norwegian-compliant invoice and sends to buyer | System (Automatic) |
| Phase 5 | Invoice Archive | View, filter, and manage all sent and received invoices | Owner/Manager |
| Phase 6 | Swap Ledger (VAT) | Track point movements with full VAT details per company | Owner/Manager |
| Phase 7 | Accounting Export | Export invoice and VAT data for Norwegian accounting software | Owner/Manager |
| Phase 8 | Invoice Routing Flow | System routes invoices between companies through SwapJoy | System (Automatic) |

---

## Phase 1: Company VAT Profile Setup (F7, F8)

**Goal:** Company owner configures VAT registration number and dedicated invoice email address

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | Owner navigates to Company Profile > VAT Settings | Display VAT Settings form |
| 1.2 | — | Load any previously saved VAT settings |
| 1.3 | Owner enters VAT/MVA number | Validate format: NO XXX XXX XXX MVA |
| 1.4 | — | Real-time format hint: "Format: NO 123 456 789 MVA" |
| 1.5 | Owner enters dedicated invoice email address | Validate email format |
| 1.6 | — | Display info text: "All invoices will be sent to this email address" |
| 1.7 | Owner clicks "Save VAT Settings" | Validate all fields |
| 1.8 | — | Save VAT number and invoice email to company profile |
| 1.9 | — | Send verification email to the invoice email address |
| 1.10 | — | Show success message: "VAT settings saved. A verification email has been sent to [email]." |
| 1.11 | Owner clicks verification link in email | Mark invoice email as verified |
| 1.12 | — | Display verified badge next to invoice email in VAT Settings |

**Success Criteria:**
- VAT/MVA number saved in correct Norwegian format (NO XXX XXX XXX MVA)
- Invoice email saved and verification email sent
- Verified invoice email displays confirmed badge
- VAT settings accessible from Company Profile page
- Company cannot register sales or receive invoices until VAT profile is complete

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Invalid MVA format | "Please enter a valid Norwegian VAT number (NO XXX XXX XXX MVA)" | Highlight field, show format example |
| Invalid email format | "Please enter a valid email address" | Highlight field |
| MVA number already registered | "This VAT number is already associated with another company" | Show warning |
| Verification email not received | "Didn't receive the email? Click to resend." | Show resend button |
| Empty MVA field | "VAT number is required" | Highlight field |
| Empty invoice email field | "Invoice email is required" | Highlight field |

---

## Phase 2: Register Sale (F14)

**Goal:** Host company (seller) registers a sale to a buyer company with VAT breakdown

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | Owner/Manager clicks "Register Sale" in sidebar or dashboard | Navigate to Register Sale form |
| 2.2 | — | Check that seller company has completed VAT profile (F7, F8) |
| 2.3 | — | If VAT profile incomplete: show warning "Please complete your VAT settings before registering a sale" with link to VAT Settings |
| 2.4 | User selects buyer company from platform list | Dropdown/searchable list of companies with verified VAT profiles |
| 2.5 | — | Display buyer company info: Name, Org Number, MVA Number |
| 2.6 | User enters sale amount in NOK (excluding VAT) | Validate positive number, min NOK 1 |
| 2.7 | User selects VAT rate | Dropdown: 25% (standard), 15% (food/beverage), 12% (transport/accommodation), 0% (exempt) |
| 2.8 | — | Auto-calculate: VAT Amount = Amount x VAT Rate |
| 2.9 | — | Auto-calculate: Total = Amount + VAT Amount |
| 2.10 | — | Display live calculation summary: Amount (ex. VAT), VAT Amount, Total (inc. VAT) |
| 2.11 | User optionally links to an experience | Dropdown of seller's experiences (optional) |
| 2.12 | User enters description (optional) | Max 500 characters, e.g. "Team dinner for 10 people" |
| 2.13 | User clicks "Preview Invoice" | Display full invoice preview (see Phase 4 for invoice format) |
| 2.14 | User reviews invoice preview | Show all invoice details: seller info, buyer info, line items, VAT breakdown, totals |
| 2.15 | User clicks "Submit & Send Invoice" | Validate all fields |
| 2.16 | — | Generate sequential invoice number (e.g., SJ-2026-00001) |
| 2.17 | — | Generate PDF invoice (F16) |
| 2.18 | — | Update points: credit seller, debit buyer (F19) |
| 2.19 | — | Send invoice PDF to buyer's invoice email (F17) |
| 2.20 | — | Store invoice in archive for both companies (F18) |
| 2.21 | — | Create ledger entries for both companies (F19) |
| 2.22 | — | Show success message: "Invoice #SJ-2026-XXXXX generated and sent to [buyer company]." |
| 2.23 | — | Redirect to Invoice Archive |

**Success Criteria:**
- Sale registered with correct VAT calculation
- Invoice generated with sequential numbering
- PDF invoice sent to buyer's verified invoice email
- Points updated for both seller and buyer
- Ledger entries created for both companies
- Invoice stored in archive for both parties
- Invoice preview matches final generated PDF

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Seller VAT profile incomplete | "Please complete your VAT settings first" | Link to VAT Settings |
| Buyer VAT profile incomplete | "The selected company has not completed their VAT registration" | Disable selection |
| No buyer selected | "Please select a buyer company" | Highlight field |
| Amount is zero or negative | "Please enter a valid amount greater than NOK 0" | Highlight field |
| No VAT rate selected | "Please select a VAT rate" | Highlight field |
| Buyer has insufficient credits | "The buyer company does not have sufficient points" | Show available balance |
| Description too long | "Description cannot exceed 500 characters" | Show character count |

---

## Phase 3: Use Points (F15)

**Note:** This is separate from the existing booking flow (Browse Marketplace -> Request -> Approve -> Redeem). The existing booking flow handles experience swapping using points. "Use Points" adds a VAT/invoice layer - when a company wants to use points and needs a proper invoice with VAT breakdown for accounting purposes. Both systems work in parallel.

**Goal:** Company uses available points toward an experience or custom amount, with a proper invoice and VAT record generated

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | Owner/Manager clicks "Use Points" in sidebar or dashboard | Navigate to Use Points form |
| 3.2 | — | Display current point balance prominently |
| 3.3 | User selects type: "Experience" or "Custom Amount" | Toggle between two modes |
| 3.4a | (Experience mode) User selects an experience from marketplace | Show experience details: name, host company, point cost, NOK value |
| 3.4b | (Custom mode) User enters custom NOK amount | Validate against available balance |
| 3.5 | — | Check available point balance >= requested amount |
| 3.6 | — | If insufficient: show "Insufficient points. Available: NOK X. Required: NOK Y." |
| 3.7 | — | Display summary: Amount to Use, Remaining Balance After |
| 3.8 | User enters purpose/note (optional) | Max 500 characters |
| 3.9 | User clicks "Confirm Points Usage" | Show confirmation dialog: "Use NOK X from your points?" |
| 3.10 | User confirms | Deduct amount from point balance |
| 3.11 | — | Create transaction record in ledger (F19) |
| 3.12 | — | If linked to experience: create corresponding invoice record |
| 3.13 | — | Show success message: "NOK X credits used. New balance: NOK Y." |
| 3.14 | — | Redirect to Swap Ledger |

**Success Criteria:**
- Credits deducted from company balance
- Transaction record created in ledger with full details
- Balance updated immediately and accurately
- Insufficient credit check prevents overspending
- Both experience-linked and custom credit usage supported

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Insufficient points | "You do not have enough credits. Available: NOK X" | Disable confirm button |
| Zero amount | "Please enter an amount greater than NOK 0" | Highlight field |
| Amount exceeds balance | "Amount exceeds available point balance" | Show max available |
| Experience unavailable | "This experience is no longer available" | Disable selection |
| No amount entered | "Please enter or select an amount" | Highlight field |

---

## Phase 4: PDF Invoice Generation & Sending (F16, F17)

**Goal:** System automatically generates a Norwegian-compliant PDF invoice and sends it to the buyer

### Phase 4A: PDF Invoice Generation (F16)

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | (Triggered by Register Sale submission) | Begin invoice generation |
| 4.2 | — | Assign sequential invoice number: SJ-YYYY-NNNNN |
| 4.3 | — | Set invoice date: current date |
| 4.4 | — | Set due date: invoice date + 14 days (configurable) |
| 4.5 | — | Populate seller information: Company name, Org number, MVA number, Address, Contact |
| 4.6 | — | Populate buyer information: Company name, Org number, MVA number, Invoice email, Address |
| 4.7 | — | Populate line items: Description, Quantity, Unit Price, VAT Rate, Line Total |
| 4.8 | — | Calculate VAT breakdown per rate (25%, 15%, 12%, 0%) |
| 4.9 | — | Calculate subtotal (ex. VAT), total VAT, grand total (inc. VAT) |
| 4.10 | — | Include payment reference and SwapJoy transaction ID |
| 4.11 | — | Generate PDF with Norwegian-compliant layout |
| 4.12 | — | Store PDF in system file storage |

**Norwegian Invoice Compliance Requirements:**

| Field | Requirement |
|-------|-------------|
| Invoice Number | Sequential, unique, no gaps (SJ-YYYY-NNNNN) |
| Invoice Date | Date of issue |
| Due Date | Payment due date |
| Seller Name | Full company name |
| Seller Org Number | Norwegian org number |
| Seller MVA Number | NO XXX XXX XXX MVA |
| Seller Address | Full registered address |
| Buyer Name | Full company name |
| Buyer Org Number | Norwegian org number |
| Buyer MVA Number | NO XXX XXX XXX MVA |
| Buyer Address | Full registered address |
| Line Items | Description, quantity, unit price |
| VAT Rate | Per line item (25%, 15%, 12%, or 0%) |
| VAT Amount | Calculated per rate |
| Subtotal | Total excluding VAT |
| Total VAT | Sum of all VAT amounts |
| Grand Total | Subtotal + Total VAT |
| Currency | NOK |
| "Merverdiavgift" | Norwegian term for VAT must appear on invoice |

### Phase 4B: Automatic Invoice Email Sending (F17)

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.13 | (Triggered after PDF generation) | Prepare email with invoice attachment |
| 4.14 | — | Set recipient: buyer's verified invoice email |
| 4.15 | — | Set subject: "Invoice #SJ-YYYY-NNNNN from [Seller Company]" |
| 4.16 | — | Set email body: Invoice summary (number, date, amount, due date) |
| 4.17 | — | Attach PDF invoice |
| 4.18 | — | Send email |
| 4.19 | — | Log email delivery status (sent/failed) |
| 4.20 | — | If delivery fails: retry up to 3 times, then flag for manual review |
| 4.21 | — | Copy email to seller company as confirmation |

**Success Criteria:**
- PDF invoice generated with all Norwegian compliance fields
- Invoice number is sequential with no gaps
- VAT breakdown is accurate per rate
- PDF emailed automatically to buyer's verified invoice email
- Delivery status tracked and logged
- Failed deliveries retried and flagged
- Both seller and buyer receive copies

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| PDF generation fails | "Invoice generation failed. Please try again." | Retry generation, log error |
| Buyer email not verified | "Buyer's invoice email is not verified" | Block sending, notify seller |
| Email delivery fails | "Invoice email could not be delivered" | Retry 3x, flag for manual review |
| Email bounce | "Invoice email bounced for [buyer company]" | Notify seller, suggest verifying buyer email |

---

## Phase 5: Invoice Archive (F18)

**Goal:** Company views, filters, and manages all sent and received invoices

| Step | User Action | System Response |
|------|-------------|-----------------|
| 5.1 | Owner/Manager clicks "Invoices" in sidebar | Navigate to Invoice Archive page |
| 5.2 | — | Load company's invoices |
| 5.3 | — | Display two tabs: "Sent Invoices" and "Received Invoices" |
| 5.4 | — | Default to "Sent Invoices" tab |
| 5.5 | — | Display invoice table: Invoice #, Date, Company, Amount (ex. VAT), VAT, Total (inc. VAT), Status |
| 5.6 | — | Display stats cards: Total Invoices, Total Amount, Pending Payment, Overdue |
| 5.7 | User clicks "Received Invoices" tab | Switch to received invoices view |
| 5.8 | — | Display same table structure for received invoices |
| 5.9 | User filters by date range | Select start and end date |
| 5.10 | User filters by company | Select company from dropdown |
| 5.11 | User filters by status | Select: All, Sent, Paid, Overdue |
| 5.12 | User searches by invoice number | Text search field |
| 5.13 | User clicks on an invoice row | Navigate to Invoice Detail view |
| 5.14 | — | Display full invoice: all header info, line items, VAT breakdown, totals, payment status |
| 5.15 | User clicks "Download PDF" | Download invoice PDF to device |
| 5.16 | User clicks "Mark as Paid" (received invoices only) | Show confirmation: "Mark invoice #X as paid?" |
| 5.17 | User confirms payment | Update invoice status to "Paid", record payment date |
| 5.18 | — | Show success message: "Invoice marked as paid." |

**Invoice Statuses:**

| Status | Description | Badge Color |
|--------|-------------|-------------|
| **Sent** | Invoice sent, awaiting payment | Blue |
| **Paid** | Payment received/confirmed | Green |
| **Overdue** | Past due date, not yet paid | Red |

**Success Criteria:**
- All sent and received invoices visible in archive
- Filters work individually and in combination
- Invoice detail shows complete information
- PDF download works for any invoice
- "Mark as Paid" updates status correctly
- Overdue invoices auto-flagged based on due date
- Stats cards show accurate totals

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No invoices found | "No invoices found" | Show empty state with explanation |
| No filter results | "No invoices match your filters" | Show clear filters button |
| PDF download fails | "Unable to download invoice. Please try again." | Retry download |

---

## Phase 6: Swap Ledger with VAT (F19)

**Goal:** Company views credit movements with full VAT details and running balance

| Step | User Action | System Response |
|------|-------------|-----------------|
| 6.1 | Owner/Manager clicks "Swap Ledger" in sidebar | Navigate to Swap Ledger page |
| 6.2 | — | Load company's points ledger with VAT details |
| 6.3 | — | Display current point balance prominently at top |
| 6.4 | — | Display ledger table: Date, Type, Company, Description, Amount (ex. VAT), VAT Amount, Total (inc. VAT), Running Balance |
| 6.5 | — | Display summary cards: Current Balance, Total Earned, Total Spent, Total VAT (Inbound), Total VAT (Outbound) |
| 6.6 | User filters by date range | Select start and end date |
| 6.7 | User filters by company | Select company from dropdown |
| 6.8 | User filters by type | Select: All, Sale (Credit), Purchase (Debit), Points Usage |
| 6.9 | User clicks on a ledger entry | Expand row to show full details: Invoice reference, VAT rate, linked experience |
| 6.10 | — | Running balance recalculated with each entry (chronological) |
| 6.11 | User views ledger pagination | Display 20 entries per page |

**Ledger Entry Types:**

| Type | Direction | Description |
|------|-----------|-------------|
| **Sale (Credit)** | + | Credits earned from a registered sale |
| **Purchase (Debit)** | - | Credits spent from a received invoice |
| **Points Usage** | - | Credits used toward an experience or custom amount |

**Success Criteria:**
- All credit movements displayed with VAT breakdown
- Running balance is accurate and updates per entry
- VAT amounts shown separately (ex. VAT, VAT amount, total inc. VAT)
- Filters work individually and in combination
- Each entry traceable to an invoice or transaction
- Ledger is append-only (immutable records)

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No ledger entries | "No transactions recorded yet" | Show empty state |
| No filter results | "No entries match your filters" | Show clear filters button |

---

## Phase 7: Accounting Export (F20)

**Goal:** Company exports invoice and VAT data for Norwegian accounting software

| Step | User Action | System Response |
|------|-------------|-----------------|
| 7.1 | Owner/Manager clicks "Export for Accounting" (from Invoices or Swap Ledger page) | Open Export dialog |
| 7.2 | User selects date range | Date picker for start and end date |
| 7.3 | User selects export type | Dropdown: All Invoices, Sent Only, Received Only, Ledger Entries |
| 7.4 | User selects format | CSV (default, compatible with Tripletex, Visma, Fiken, etc.) |
| 7.5 | — | Display preview: "X records found for the selected period" |
| 7.6 | User clicks "Download Export" | Generate CSV file |
| 7.7 | — | CSV includes: Invoice Number, Invoice Date, Due Date, Seller Name, Seller Org Number, Seller MVA Number, Buyer Name, Buyer Org Number, Buyer MVA Number, Description, Amount (ex. VAT), VAT Rate, VAT Amount, Total (inc. VAT), Currency (NOK), Status |
| 7.8 | — | Download CSV file to device |
| 7.9 | — | Show success message: "Export complete. X records downloaded." |

**CSV Column Specification:**

| Column | Description | Example |
|--------|-------------|---------|
| Invoice Number | Unique invoice reference | SJ-2026-00001 |
| Invoice Date | Date invoice was issued | 2026-04-12 |
| Due Date | Payment due date | 2026-04-26 |
| Seller Name | Selling company name | Nordic Adventures AS |
| Seller Org No | Seller org number | 912 345 678 |
| Seller MVA No | Seller VAT number | NO 912 345 678 MVA |
| Buyer Name | Buying company name | Oslo Events AS |
| Buyer Org No | Buyer org number | 987 654 321 |
| Buyer MVA No | Buyer VAT number | NO 987 654 321 MVA |
| Description | Line item description | Spa Day Package for 5 |
| Amount Ex. VAT | Amount excluding VAT | 10000.00 |
| VAT Rate | Applied VAT rate | 25% |
| VAT Amount | Calculated VAT | 2500.00 |
| Total Inc. VAT | Grand total | 12500.00 |
| Currency | Always NOK | NOK |
| Status | Invoice status | Paid |

**Success Criteria:**
- CSV export includes all required fields for Norwegian accounting
- Data compatible with Tripletex, Visma, Fiken, and other Norwegian software
- Date range filter works correctly
- Export type filter works correctly
- File downloads successfully with correct naming: `swapjoy-export-YYYY-MM-DD.csv`
- Empty exports handled gracefully

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| No data in range | "No records found for the selected date range" | Disable download button |
| Export generation fails | "Export failed. Please try again." | Retry option |
| Date range invalid | "Start date must be before end date" | Highlight fields |

---

## Phase 8: Invoice Routing Flow (F21)

**Goal:** System correctly routes invoices between companies through SwapJoy when experiences are redeemed

### Phase 8A: Automatic Invoice Routing on Experience Redemption

| Step | User Action | System Response |
|------|-------------|-----------------|
| 8.1 | Experience is redeemed (QR scanned / code entered) | Trigger invoice routing logic |
| 8.2 | — | Identify host company (seller) and requesting company (buyer) |
| 8.3 | — | Verify both companies have completed VAT profiles |
| 8.4 | — | Determine invoice amount based on experience value and applicable VAT rate |
| 8.5 | — | Generate invoice from host company (seller) to buyer company |
| 8.6 | — | Apply invoice routing: Host Company -> SwapJoy Platform -> Buyer Company |
| 8.7 | — | Generate PDF invoice (F16) |
| 8.8 | — | Send invoice to buyer's invoice email (F17) |
| 8.9 | — | Update points for both companies (F19) |
| 8.10 | — | Create ledger entries for both companies (F19) |
| 8.11 | — | Store invoice in archive for both companies (F18) |
| 8.12 | — | Log routing details and delivery status |

### Phase 8B: Manual Sale Registration Routing

| Step | User Action | System Response |
|------|-------------|-----------------|
| 8.13 | Seller registers a sale via Register Sale form (F14) | Trigger invoice routing |
| 8.14 | — | Generate invoice from seller to buyer |
| 8.15 | — | Route invoice through SwapJoy platform |
| 8.16 | — | Same processing as steps 8.7 through 8.12 |

### Invoice Routing Diagram

```
EXPERIENCE REDEMPTION FLOW:
============================================================

  Host Company (Seller)          SwapJoy Platform           Buyer Company
  ========================       ===================        =======================
  
  1. Experience redeemed   --->  2. Determine invoice  ---> 
                                    flow & amounts
                                                      
  3. Invoice generated     <---  4. Route invoice      ---> 5. Invoice received
     (appears in Sent            through platform           (appears in Received
      Invoices archive)                                      Invoices archive)
                                                      
                                 6. Send PDF to buyer  ---> 7. PDF arrives at
                                    invoice email            invoice email
                                                      
  8. Credits earned        <---  9. Update swap        ---> 10. Credits debited
     (+ balance)                    credits for both         (- balance)
                                                      
  11. Ledger entry         <--- 12. Create ledger      ---> 13. Ledger entry
      created (credit)              entries for both          created (debit)

============================================================

MANUAL SALE REGISTRATION FLOW:
============================================================

  Seller Company                 SwapJoy Platform           Buyer Company
  ========================       ===================        =======================
  
  1. Clicks "Register     --->  2. Validate sale
     Sale", fills form          3. Generate invoice #
                                                      
  4. Preview invoice       <---  5. Show preview       
                                                      
  6. Confirms "Submit      ---> 7. Generate PDF        ---> 8. Invoice received
     & Send Invoice"            8. Route to buyer            (appears in archive)
                                                      
                                 9. Email PDF           ---> 10. PDF arrives at
                                    to buyer                  invoice email
                                                      
  11. Credits earned       <--- 12. Update swap        ---> 13. Credits debited
      (+ balance)                   credits for both          (- balance)
                                                      
  14. Ledger entry         <--- 15. Create ledger      ---> 16. Ledger entry
      created (credit)              entries for both          created (debit)

============================================================
```

**Success Criteria:**
- Automatic routing triggered on experience redemption
- Manual routing triggered on Register Sale submission
- Both companies see the invoice in their respective archives
- Credits updated accurately for both parties
- Ledger entries created for both companies
- PDF sent to correct invoice email
- Full audit trail of routing maintained

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Buyer VAT profile incomplete | "Cannot route invoice. Buyer has not completed VAT registration." | Notify seller, hold invoice |
| Seller VAT profile incomplete | "Cannot generate invoice. Please complete your VAT settings." | Block routing, prompt setup |
| Routing fails | "Invoice routing failed. Invoice saved as draft." | Save as draft, flag for manual review |
| Buyer email unverified | "Buyer's invoice email is not verified. Invoice stored but not emailed." | Store in archive, notify parties |

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | VAT Settings | Company Profile > VAT Settings | Save -> Company Profile |
| 2 | Register Sale Form | Sidebar "Register Sale" / Dashboard | Preview -> Submit -> Invoice Archive |
| 3 | Invoice Preview | "Preview Invoice" in Register Sale | Back -> Register Sale / Submit -> Send |
| 4 | Use Points Form | Sidebar "Use Points" / Dashboard | Confirm -> Swap Ledger |
| 5 | Invoice Archive (Sent) | Sidebar "Invoices" | Click row -> Invoice Detail |
| 6 | Invoice Archive (Received) | Sidebar "Invoices" > Received tab | Click row -> Invoice Detail |
| 7 | Invoice Detail | Click invoice row in archive | Download PDF / Mark as Paid / Back |
| 8 | Swap Ledger | Sidebar "Swap Ledger" | Click entry -> Detail / Export |
| 9 | Accounting Export Dialog | "Export for Accounting" button | Download CSV / Cancel |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| MVA Number | Required, Format: NO XXX XXX XXX MVA, unique per company |
| Invoice Email | Required, valid email format, must be verified |
| Buyer Company | Required, must have completed VAT profile |
| Sale Amount (NOK) | Required, positive number, minimum NOK 1 |
| VAT Rate | Required, one of: 25%, 15%, 12%, 0% |
| Points Usage Amount | Required, positive number, cannot exceed available balance |
| Export Date Range | Optional, start date <= end date |
| Invoice Description | Optional, max 500 characters |
| Points Usage Note | Optional, max 500 characters |
| Invoice Status Change | Only "Mark as Paid" allowed (received invoices only) |

---

## Navigation Changes

### Company User (Owner/Manager) Sidebar
**MAIN MENU:**
- Dashboard (fa-th-large)
- Experiences (fa-store)
- My Bookings (fa-ticket-alt)
- Points & Balance (fa-coins)

**MANAGEMENT:**
- Employees (fa-users)
- My Experiences (fa-calendar-plus)
- Redeem Ticket (fa-keyboard)
- Tax Reports (fa-file-invoice)
- **Invoices** (fa-file-invoice-dollar) - new
- **Register Sale** (fa-cash-register) - new
- **Swap Ledger** (fa-book) - new

**Header Profile Dropdown:**
- Company Profile (includes **VAT Settings** tab - F7, F8)
- Settings

### SwapJoys Admin Sidebar
**ADMIN PANEL:**
- Dashboard (fa-th-large)
- Companies (fa-building)
- Experiences (fa-star)
- Usage Logs (fa-chart-bar)
- Point Adjustments (fa-sliders-h)

---

## Role-Based Access

| Action | Owner | Manager | Employee | SwapJoys Admin |
|--------|:-----:|:-------:|:--------:|:--------------:|
| Configure VAT Settings (F7, F8) | Yes | - | - | - |
| Register Sale (F14) | Yes | Yes | - | - |
| Use Points (F15) | Yes | Yes | - | - |
| View Invoice Preview | Yes | Yes | - | - |
| View Invoice Archive (F18) | Yes | Yes | - | - |
| Download Invoice PDF (F16) | Yes | Yes | - | - |
| Mark Invoice as Paid | Yes | Yes | - | - |
| View Swap Ledger (F19) | Yes | Yes | - | - |
| Export Accounting Data (F20) | Yes | Yes | - | - |
| Receive Invoice Email (F17) | Yes | Yes | - | - |
| View Platform-Wide Invoices | - | - | - | Yes |
| View Platform VAT Reports | - | - | - | Yes |

---

## Example Invoice Flow

**Scenario:** Nordic Adventures AS hosts a team dinner experience for Oslo Events AS

```
Step 1: REGISTER SALE
------------------------------------------------------------
Nordic Adventures AS (Seller) clicks "Register Sale"
  - Selects buyer: Oslo Events AS
  - Amount: NOK 10,000 (ex. VAT)
  - VAT Rate: 15% (food/beverage)
  - Description: "Team dinner experience for 10 guests"

Step 2: CALCULATION
------------------------------------------------------------
  Amount (ex. VAT):     NOK 10,000.00
  VAT (15%):            NOK  1,500.00
  Total (inc. VAT):     NOK 11,500.00

Step 3: INVOICE GENERATED
------------------------------------------------------------
  Invoice #:            SJ-2026-00042
  Date:                 2026-04-12
  Due Date:             2026-04-26
  
  FROM:                 Nordic Adventures AS
                        Org: 912 345 678
                        MVA: NO 912 345 678 MVA
  
  TO:                   Oslo Events AS
                        Org: 987 654 321
                        MVA: NO 987 654 321 MVA
  
  ITEM                  QTY    PRICE       VAT     TOTAL
  Team dinner (10)      1      10,000.00   15%     11,500.00
  
  Subtotal (ex. MVA):                      NOK 10,000.00
  Merverdiavgift (15%):                    NOK  1,500.00
  TOTAL:                                   NOK 11,500.00

Step 4: AUTOMATED ACTIONS
------------------------------------------------------------
  [x] PDF generated and stored
  [x] Email sent to: invoices@osloevents.no
  [x] Nordic Adventures AS: +10,000 credits (Swap Ledger)
  [x] Oslo Events AS: -10,000 credits (Swap Ledger)
  [x] Invoice appears in Nordic Adventures "Sent" archive
  [x] Invoice appears in Oslo Events "Received" archive
  [x] Ledger entries created for both companies

Step 5: POST-INVOICE
------------------------------------------------------------
  Oslo Events AS marks invoice as "Paid"
  -> Status changes: Sent -> Paid
  -> Payment date recorded
```

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform  
**Module:** VAT / Invoicing (Features 7, 8, 14, 15, 16, 17, 18, 19, 20, 21)
