# SwapJoys Platform - Wireframes
## VAT / Invoicing Module (Features 7, 8, 14, 15, 16, 17, 18, 19, 20, 21)

| | |
|---|---|
| **Project** | SwapJoys Platform |
| **Module** | VAT / Invoicing |
| **Prepared by** | Rebing Tech |
| **Date** | April 2026 |
| **Status** | Ready for Client Review |

---

## Screen Overview

| # | Screen | Description | Actor |
|---|--------|-------------|-------|
| 1 | Company VAT Settings | VAT/MVA number and invoice email configuration | Owner/Manager |
| 2 | Register Sale Form | Create a new sale transaction with VAT calculation | Owner/Manager |
| 3 | Use Points Form | Spend points toward experiences or custom amounts | Owner/Manager |
| 4 | Invoice Preview / PDF Layout | Norwegian-compliant invoice document layout | Owner/Manager |
| 5 | Invoice Archive - Sent | List of all outgoing invoices with filters | Owner/Manager |
| 6 | Invoice Archive - Received | List of all incoming invoices with actions | Owner/Manager |
| 7 | Invoice Detail View | Full detail view of a single invoice | Owner/Manager |
| 8 | Swap Ledger (VAT Credits) | Credit balance and transaction history | Owner/Manager |
| 9 | Accounting Export | Export data for Norwegian accounting software | Owner/Manager |
| 10 | Register Sale Confirmation | Success screen after sale registration | Owner/Manager |

---

## 1. Company VAT Settings (F7, F8)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  COMPANY PROFILE                              |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Company Profile                                              |
|                  |  Manage your company information and VAT settings              |
| -------------    |                                                                |
|                  |  [Company Info]  [VAT Settings]                                |
| MAIN MENU        |                                                                |
|                  |  +------------------------------------------------------------+|
| # Dashboard      |  |                                                            ||
| # Experiences    |  |  VAT / Invoice Settings                                    ||
| # My Bookings    |  |  --------------------------------------------------------  ||
| # Points &       |  |                                                            ||
|   Balance        |  |  VAT/MVA Number *                                          ||
|                  |  |  +------------------------------------------------------+  ||
| MANAGEMENT       |  |  | NO 123 456 789 MVA                                  |  ||
| # Invoices       |  |  +------------------------------------------------------+  ||
| # Register Sale  |  |  Format: NO XXX XXX XXX MVA                               ||
| # Swap Ledger    |  |                                                            ||
| # Employees      |  |  Invoice Email *                                           ||
| # My Experiences |  |  +------------------------------------------------------+  ||
| # Tax Reports    |  |  | faktura@techcorp.no                                  |  ||
| # Settings       |  |  +------------------------------------------------------+  ||
|                  |  |  Invoices will be sent to this email address                ||
|                  |  |                                                            ||
|                  |  |  Company Name (from profile)                                ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | TechCorp AS                                          |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  (Read-only, edit in Company Info tab)                      ||
|                  |  |                                                            ||
|                  |  |  Organization Number (from profile)                         ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | 912 345 678                                          |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  (Read-only, edit in Company Info tab)                      ||
|                  |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |                              [Cancel]    [Save Settings]    ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Tab Navigation | Company Info / VAT Settings tabs |
| VAT/MVA Number | Text input, format NO XXX XXX XXX MVA, validated on save |
| Invoice Email | Email input, used as the default email for receiving invoices |
| Company Name | Read-only display from company profile |
| Organization Number | Read-only display from company profile |
| Cancel Button | Discard changes, return to previous state |
| Save Settings Button | Validate and persist VAT settings |
| Sidebar - Invoices | New menu item under MANAGEMENT section |
| Sidebar - Register Sale | New menu item under MANAGEMENT section |
| Sidebar - Swap Ledger | New menu item under MANAGEMENT section |

---

## 2. Register Sale Form (F14)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  REGISTER SALE                                 |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Register Sale                                                |
|                  |  Create a new sale and generate an invoice                     |
| -------------    |                                                                |
|                  |  +------------------------------------------------------------+|
| MAIN MENU        |  |                                                            ||
|                  |  |  Buyer Company *                                            ||
| # Dashboard      |  |  +------------------------------------------------------+  ||
| # Experiences    |  |  | Select a company...                              v   |  ||
| # My Bookings    |  |  +------------------------------------------------------+  ||
| # Points &       |  |                                                            ||
|   Balance        |  |  Amount (NOK) *                                            ||
|                  |  |  +------------------------------------------------------+  ||
| MANAGEMENT       |  |  | 10,000.00                                            |  ||
| # Invoices       |  |  +------------------------------------------------------+  ||
| # Register Sale <|  |                                                            ||
| # Swap Ledger    |  |  VAT Rate *                                                ||
| # Employees      |  |  +------------------------------------------------------+  ||
| # My Experiences |  |  | 25% - Standard                                   v   |  ||
| # Tax Reports    |  |  +------------------------------------------------------+  ||
| # Settings       |  |  Options:                                                  ||
|                  |  |    25% - Standard                                           ||
|                  |  |    15% - Food & Drink                                       ||
|                  |  |    12% - Transport & Hotels                                 ||
|                  |  |     0% - Exempt                                             ||
|                  |  |                                                            ||
|                  |  |  Description / Notes                                       ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Team building experience - April 2026               |  ||
|                  |  |  |                                                      |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  Link to Experience (optional)                              ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Spa Day Package                                  v   |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  |  Calculation Preview                                 |  ||
|                  |  |  |  --------------------------------------------------- |  ||
|                  |  |  |                                                      |  ||
|                  |  |  |  Amount ex. VAT:          NOK  8,000.00              |  ||
|                  |  |  |  VAT Amount (25%):        NOK  2,000.00              |  ||
|                  |  |  |  ─────────────────────────────────────               |  ||
|                  |  |  |  Total incl. VAT:         NOK 10,000.00              |  ||
|                  |  |  |                                                      |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |                              [Cancel]    [Submit Sale]      ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Buyer Company Dropdown | Searchable dropdown of all platform companies |
| Amount (NOK) Input | Numeric input for total sale amount including VAT |
| VAT Rate Dropdown | 25% Standard, 15% Food & Drink, 12% Transport & Hotels, 0% Exempt |
| Description / Notes | Free-text textarea for sale description |
| Link to Experience | Optional dropdown of seller's active experiences |
| Calculation Preview | Live-calculated box showing Amount ex. VAT, VAT Amount, Total |
| Cancel Button | Discard and return to previous page |
| Submit Sale Button | Validate inputs, create sale, and generate invoice |

---

## 3. Use Points Form (F15)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  USE CREDITS                                   |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Use Points                                                  |
|                  |  Spend your points                                      |
| -------------    |                                                                |
|                  |  +------------------------------------------------------------+|
| MAIN MENU        |  |                                                            ||
|                  |  |  +------------------------------------------------------+  ||
| # Dashboard      |  |  |                                                      |  ||
| # Experiences    |  |  |      Current Credit Balance                          |  ||
| # My Bookings    |  |  |                                                      |  ||
| # Points &       |  |  |         NOK 24,500.00                                |  ||
|   Balance        |  |  |                                                      |  ||
|                  |  |  |      Available for use                                |  ||
| MANAGEMENT       |  |  |                                                      |  ||
| # Invoices       |  |  +------------------------------------------------------+  ||
| # Register Sale  |  |                                                            ||
| # Swap Ledger    |  |  Select Experience (optional)                              ||
| # Employees      |  |  +------------------------------------------------------+  ||
| # My Experiences |  |  | Choose an experience...                          v   |  ||
| # Tax Reports    |  |  +------------------------------------------------------+  ||
| # Settings       |  |                                                            ||
|                  |  |  -- OR --                                                   ||
|                  |  |                                                            ||
|                  |  |  Custom Amount (NOK) *                                     ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | 5,000.00                                             |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  |                                                      |  ||
|                  |  |  |  Balance Check                                       |  ||
|                  |  |  |  --------------------------------------------------- |  ||
|                  |  |  |                                                      |  ||
|                  |  |  |  Current Balance:       NOK 24,500.00                |  ||
|                  |  |  |  Amount to Use:         NOK  5,000.00                |  ||
|                  |  |  |  Remaining Balance:     NOK 19,500.00                |  ||
|                  |  |  |                                                      |  ||
|                  |  |  |  Status:  [Sufficient Balance]                       |  ||
|                  |  |  |                                                      |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |                              [Cancel]    [Confirm Usage]    ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Credit Balance Card | Large, prominent display of current NOK point balance |
| Select Experience Dropdown | Optional dropdown of available experiences with their values |
| Custom Amount Input | Numeric input for a custom credit usage amount |
| Balance Check Box | Live calculation: Current Balance, Amount to Use, Remaining Balance |
| Sufficient/Insufficient Indicator | Green "Sufficient Balance" or Red "Insufficient Balance" badge |
| Cancel Button | Discard and return to previous page |
| Confirm Usage Button | Disabled if insufficient balance; submits credit usage |

---

## 4. Invoice Preview / PDF Layout (F16)

```
+-----------------------------------------------------------------+
|                                                                   |
|  +-----------------------------------------------------------+   |
|  |                                                           |   |
|  |  [SwapJoy Logo]                                          |   |
|  |                                                           |   |
|  |                               FAKTURA / INVOICE           |   |
|  |                                                           |   |
|  |  Invoice #:  SJ-2026-0042                                |   |
|  |  Date:       April 10, 2026                               |   |
|  |  Due Date:   April 24, 2026                               |   |
|  |                                                           |   |
|  |  -----------------------------------------------------------  |
|  |                                                           |   |
|  |  SELLER                        BUYER                      |   |
|  |  +------------------------+   +------------------------+  |   |
|  |  | TechCorp AS            |   | Nordic Wellness AS     |  |   |
|  |  | Org.nr: 912 345 678    |   | Org.nr: 923 456 789   |  |   |
|  |  | MVA: NO 912 345 678 MVA|   | MVA: NO 923 456 789 MVA| |   |
|  |  | Storgata 1             |   | Fjordveien 12          |  |   |
|  |  | 5003 Bergen            |   | 0150 Oslo              |  |   |
|  |  | ola@techcorp.no        |   | post@nordicwell.no     |  |   |
|  |  +------------------------+   +------------------------+  |   |
|  |                                                           |   |
|  |  -----------------------------------------------------------  |
|  |                                                           |   |
|  |  LINE ITEMS                                               |   |
|  |  +-------------------------------------------------------+   |
|  |  | #  | DESCRIPTION          | QTY | UNIT PRICE | VAT  | AMOUNT  |
|  |  +-------------------------------------------------------+   |
|  |  | 1  | Spa Day Package      |  1  |  8,000.00  | 25%  | 8,000.00|
|  |  +-------------------------------------------------------+   |
|  |  | 2  | Catering Lunch       |  1  |  2,608.70  | 15%  | 2,608.70|
|  |  +-------------------------------------------------------+   |
|  |  | 3  | Transport Arrangement|  1  |  1,785.71  | 12%  | 1,785.71|
|  |  +-------------------------------------------------------+   |
|  |                                                           |   |
|  |  -----------------------------------------------------------  |
|  |                                                           |   |
|  |  SUMMARY                                                  |   |
|  |  +-------------------------------------------------------+   |
|  |  |                                                       |   |
|  |  |  Subtotal (ex. VAT):                    NOK 12,394.41 |   |
|  |  |                                                       |   |
|  |  |  VAT 25% (of NOK 8,000.00):            NOK  2,000.00 |   |
|  |  |  VAT 15% (of NOK 2,608.70):            NOK    391.30 |   |
|  |  |  VAT 12% (of NOK 1,785.71):            NOK    214.29 |   |
|  |  |  ─────────────────────────────────────────────────     |   |
|  |  |  Total VAT:                             NOK  2,605.59 |   |
|  |  |                                                       |   |
|  |  |  =====================================================|   |
|  |  |  TOTAL AMOUNT:                          NOK 15,000.00 |   |
|  |  |  =====================================================|   |
|  |  |                                                       |   |
|  |  +-------------------------------------------------------+   |
|  |                                                           |   |
|  |  -----------------------------------------------------------  |
|  |                                                           |   |
|  |  PAYMENT INFORMATION                                      |   |
|  |  Payment Terms:  14 days net                              |   |
|  |  Bank:           DNB                                      |   |
|  |  Account:        1234 56 78901                            |   |
|  |  IBAN:           NO12 1234 5678 901                       |   |
|  |  SWIFT/BIC:      DNBANOKK                                |   |
|  |                                                           |   |
|  |  -----------------------------------------------------------  |
|  |                                                           |   |
|  |  This invoice is generated via the SwapJoys platform.     |   |
|  |  Registered in Bronnoysundregistrene.                     |   |
|  |  All amounts in NOK.                                      |   |
|  |                                                           |   |
|  +-----------------------------------------------------------+   |
|                                                                   |
+-----------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| SwapJoy Logo | Platform logo in top-left corner |
| Invoice Title | "FAKTURA / INVOICE" prominently displayed |
| Invoice Number | Format SJ-YYYY-NNNN (e.g., SJ-2026-0042) |
| Date / Due Date | Invoice issue date and payment due date |
| Seller Info Card | Company name, Org number, MVA number, address, email |
| Buyer Info Card | Company name, Org number, MVA number, address, invoice email |
| Line Items Table | Row number, Description, Quantity, Unit Price (ex. VAT), VAT Rate, Amount (ex. VAT) |
| VAT Summary | Subtotal, per-rate VAT breakdown, Total VAT, Grand Total |
| Payment Information | Payment terms, bank name, account number, IBAN, SWIFT/BIC |
| Footer Legal Text | Platform reference, registration note, currency note |

---

## 5. Invoice Archive - Sent (F18)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  INVOICES                                      |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Invoices                                                     |
|                  |  Manage your sent and received invoices                        |
| -------------    |                                                                |
|                  |  [Sent Invoices]  [Received Invoices]                          |
| MAIN MENU        |                                                                |
|                  |  +------------------------------------------------------------+|
| # Dashboard      |  |                                                            ||
| # Experiences    |  | [Search...       ]  [All Companies v]  [All Status v]      ||
| # My Bookings    |  | [Date From  ]  [Date To  ]                                ||
| # Points &       |  |                                                            ||
|   Balance        |  | +--------------------------------------------------------+ ||
|                  |  | | INVOICE # | DATE     | BUYER       | AMOUNT  | VAT    | ||
| MANAGEMENT       |  | |           |          | COMPANY     | EX. VAT | AMOUNT | ||
| # Invoices    <  |  | |           |          |             |         | TOTAL  | ||
| # Register Sale  |  | |           |          |             |         | STATUS | ||
| # Swap Ledger    |  | +--------------------------------------------------------+ ||
| # Employees      |  | | SJ-2026-  | Apr 10   | Nordic      | 8,000   | 2,000  | ||
| # My Experiences |  | | 0042      | 2026     | Wellness AS | 10,000  | [Sent] | ||
| # Tax Reports    |  | +--------------------------------------------------------+ ||
| # Settings       |  | | SJ-2026-  | Apr 07   | FoodCorp AS | 6,400   | 960    | ||
|                  |  | | 0038      | 2026     |             |  7,360  | [Paid] | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | SJ-2026-  | Mar 28   | FitNord AS  | 4,000   | 1,000  | ||
|                  |  | | 0031      | 2026     |             |  5,000  |[Overdue]| ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | SJ-2026-  | Mar 20   | Bergen      | 3,200   | 800    | ||
|                  |  | | 0025      | 2026     | Events AS   |  4,000  | [Paid] | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  |                  [1] [2] [3] ... [Next]                     ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Tab Navigation | Sent Invoices (active) / Received Invoices |
| Search Box | Filter by invoice number, company name |
| Company Filter | Dropdown of buyer companies |
| Status Filter | All, Sent, Paid, Overdue |
| Date Range | From / To date pickers |
| Invoice Table | Invoice #, Date, Buyer Company, Amount ex. VAT, VAT Amount, Total, Status |
| Status Badges | Sent (blue), Paid (green), Overdue (red) |
| Row Click | Navigate to Invoice Detail view |
| Pagination | 20 invoices per page |

---

## 6. Invoice Archive - Received (F18)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  INVOICES                                      |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Invoices                                                     |
|                  |  Manage your sent and received invoices                        |
| -------------    |                                                                |
|                  |  [Sent Invoices]  [Received Invoices]                          |
| MAIN MENU        |                                                                |
|                  |  +------------------------------------------------------------+|
| # Dashboard      |  |                                                            ||
| # Experiences    |  | [Search...       ]  [All Companies v]  [All Status v]      ||
| # My Bookings    |  | [Date From  ]  [Date To  ]                                ||
| # Points &       |  |                                                            ||
|   Balance        |  | +--------------------------------------------------------+ ||
|                  |  | | INVOICE # | DATE     | SELLER      | AMOUNT  | VAT    | ||
| MANAGEMENT       |  | |           |          | COMPANY     | EX. VAT | AMOUNT | ||
| # Invoices    <  |  | |           |          |             |         | TOTAL  | ||
| # Register Sale  |  | |           |          |             |         | STATUS | ||
| # Swap Ledger    |  | |           |          |             |         | ACTIONS| ||
| # Employees      |  | +--------------------------------------------------------+ ||
| # My Experiences |  | | SJ-2026-  | Apr 10   | TechCorp AS | 8,000   | 2,000  | ||
| # Tax Reports    |  | | 0042      | 2026     |             | 10,000  | [Sent] | ||
| # Settings       |  | |           |          |             |         |[Mark   || ||
|                  |  | |           |          |             |         | Paid]  | ||
|                  |  | |           |          |             |         |[PDF]   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | SJ-2026-  | Apr 05   | FoodCorp AS | 5,200   | 780    | ||
|                  |  | | 0036      | 2026     |             |  5,980  | [Paid] | ||
|                  |  | |           |          |             |         |[PDF]   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | SJ-2026-  | Mar 25   | FitNord AS  | 3,600   | 900    | ||
|                  |  | | 0029      | 2026     |             |  4,500  |[Overdue]| ||
|                  |  | |           |          |             |         |[Mark   || ||
|                  |  | |           |          |             |         | Paid]  | ||
|                  |  | |           |          |             |         |[PDF]   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  |                  [1] [2] [3] ... [Next]                     ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Tab Navigation | Sent Invoices / Received Invoices (active) |
| Search Box | Filter by invoice number, company name |
| Company Filter | Dropdown of seller companies |
| Status Filter | All, Sent, Paid, Overdue |
| Date Range | From / To date pickers |
| Invoice Table | Invoice #, Date, Seller Company, Amount ex. VAT, VAT Amount, Total, Status, Actions |
| Status Badges | Sent (blue), Paid (green), Overdue (red) |
| Mark as Paid Button | Changes invoice status to Paid; visible for Sent and Overdue invoices |
| Download PDF Button | Downloads the invoice as a PDF file |
| Row Click | Navigate to Invoice Detail view |
| Pagination | 20 invoices per page |

---

## 7. Invoice Detail View (F18)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  INVOICE DETAIL                                |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  <- Back to Invoices                                          |
|                  |                                                                |
| -------------    |  +------------------------------------------------------------+|
|                  |  |                                                            ||
| MANAGEMENT       |  |  Invoice SJ-2026-0042                          [Sent]     ||
| # Invoices    <  |  |  Issued: April 10, 2026                                   ||
| # Register Sale  |  |  Due: April 24, 2026                                      ||
| # Swap Ledger    |  |                                                            ||
|                  |  |  [Download PDF]    [Mark as Paid]                           ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
|                  |  +---------------------------+  +---------------------------+  |
|                  |  | SELLER                    |  | BUYER                     |  |
|                  |  | -------------------------  |  | -------------------------  |  |
|                  |  |                           |  |                           |  |
|                  |  | TechCorp AS               |  | Nordic Wellness AS        |  |
|                  |  | Org.nr: 912 345 678       |  | Org.nr: 923 456 789       |  |
|                  |  | MVA: NO 912 345 678 MVA   |  | MVA: NO 923 456 789 MVA   |  |
|                  |  | Storgata 1, 5003 Bergen   |  | Fjordveien 12, 0150 Oslo  |  |
|                  |  | ola@techcorp.no           |  | post@nordicwell.no        |  |
|                  |  |                           |  |                           |  |
|                  |  +---------------------------+  +---------------------------+  |
|                  |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  | LINE ITEMS                                                ||
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | #  | DESCRIPTION          | QTY | UNIT PRICE | VAT | AMT  ||
|                  |  | ---+----------------------+-----+------------+-----+----- ||
|                  |  | 1  | Spa Day Package      |  1  |  8,000.00  | 25% |8,000 ||
|                  |  | ---+----------------------+-----+------------+-----+----- ||
|                  |  | 2  | Catering Lunch       |  1  |  2,608.70  | 15% |2,609 ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  | VAT BREAKDOWN                                              ||
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  |  Subtotal (ex. VAT):                      NOK 10,608.70    ||
|                  |  |                                                            ||
|                  |  |  VAT 25% (of NOK 8,000.00):               NOK  2,000.00    ||
|                  |  |  VAT 15% (of NOK 2,608.70):               NOK    391.30    ||
|                  |  |  ─────────────────────────────────────────────────          ||
|                  |  |  Total VAT:                                NOK  2,391.30    ||
|                  |  |                                                            ||
|                  |  |  =============================================              ||
|                  |  |  TOTAL:                                    NOK 13,000.00    ||
|                  |  |  =============================================              ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | Return to Invoices list |
| Invoice Header | Invoice number, issue date, due date, status badge |
| Download PDF Button | Generate and download the invoice as PDF |
| Mark as Paid Button | Change status to Paid (visible for received invoices with Sent/Overdue status) |
| Seller Info Card | Company name, org number, MVA number, address, email |
| Buyer Info Card | Company name, org number, MVA number, address, email |
| Line Items Table | Row number, Description, Quantity, Unit Price, VAT Rate, Amount |
| VAT Breakdown | Subtotal, per-rate VAT amounts, Total VAT, Grand Total |

---

## 8. Swap Ledger - VAT Credits (F19)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  SWAP LEDGER                                   |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Swap Ledger                                                  |
|                  |  Track your VAT point balance and activity                    |
| -------------    |                                                                |
|                  |  +------------------+  +------------------+  +------------------+
| MAIN MENU        |  |                  |  |                  |  |                  |
|                  |  |  NOK 24,500.00   |  |  NOK 38,000.00   |  |  NOK 13,500.00   |
| # Dashboard      |  |                  |  |                  |  |                  |
| # Experiences    |  |  Current Credit  |  |  Total Credits   |  |  Total Credits   |
| # My Bookings    |  |  Balance         |  |  Earned          |  |  Used            |
| # Points &       |  |                  |  |                  |  |                  |
|   Balance        |  +------------------+  +------------------+  +------------------+
|                  |                                                                |
| MANAGEMENT       |  +------------------------------------------------------------+|
| # Invoices       |  |                                                            ||
| # Register Sale  |  | [All Companies v]  [All Types v]  [Date From] [Date To]    ||
| # Swap Ledger <  |  |                                                            ||
| # Employees      |  | +--------------------------------------------------------+ ||
| # My Experiences |  | | DATE     | TYPE           | COMPANY      | AMOUNT   | VAT     | ||
| # Tax Reports    |  | |          |                |              | EX. VAT  | AMOUNT  | ||
| # Settings       |  | |          |                |              | TOTAL    | BALANCE | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 10   | Credit Earned  | Nordic       | 8,000    | 2,000   | ||
|                  |  | | 2026     |                | Wellness AS  | 10,000   | 24,500  | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 07   | Credit Earned  | FoodCorp AS  | 5,200    |   780   | ||
|                  |  | | 2026     |                |              |  5,980   | 14,500  | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 03   | Credit Used    | FitNord AS   | 4,000    | 1,000   | ||
|                  |  | | 2026     |                |              |  5,000   |  8,520  | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Mar 28   | Credit Earned  | Bergen       | 3,200    |   800   | ||
|                  |  | | 2026     |                | Events AS    |  4,000   | 13,520  | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Mar 20   | Credit Used    | TechCorp AS  | 2,400    |   600   | ||
|                  |  | | 2026     |                |              |  3,000   |  9,520  | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  |                  [1] [2] [3] ... [Next]                     ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Current Credit Balance Card | Large, prominent display of current NOK balance |
| Total Credits Earned Card | Sum of all credits received, green accent |
| Total Credits Used Card | Sum of all credits spent, orange accent |
| Company Filter | Dropdown to filter by counterpart company |
| Type Filter | All, Credit Earned, Credit Used |
| Date Range | From / To date pickers |
| Ledger Table | Date, Type, Company, Amount ex. VAT, VAT Amount, Total, Running Balance |
| Credit Earned Rows | Green indicator for incoming credits |
| Credit Used Rows | Red indicator for outgoing credits |
| Pagination | 20 entries per page |

---

## 9. Accounting Export (F20)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  ACCOUNTING EXPORT                              |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Accounting Export                                             |
|                  |  Export transaction data for your accounting software           |
| -------------    |                                                                |
|                  |  +------------------------------------------------------------+|
| MAIN MENU        |  |                                                            ||
|                  |  |  Compatible with Tripletex, Visma, and other Norwegian     ||
| # Dashboard      |  |  accounting software.                                      ||
| # Experiences    |  |                                                            ||
| # My Bookings    |  |  --------------------------------------------------------  ||
| # Points &       |  |                                                            ||
|   Balance        |  |  Date Range *                                              ||
|                  |  |  [Apr 01, 2026  ]  to  [Apr 30, 2026  ]                    ||
| MANAGEMENT       |  |                                                            ||
| # Invoices       |  |  --------------------------------------------------------  ||
| # Register Sale  |  |                                                            ||
| # Swap Ledger    |  |  Export Preview (12 transactions found)                    ||
| # Employees      |  |                                                            ||
| # My Experiences |  |  +------------------------------------------------------+  ||
| # Tax Reports    |  |  | DATE     | DOC #       | ACCOUNT | DESCRIPTION | AMOUNT|  ||
| # Settings       |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 10   | SJ-2026-0042| 3000    | Sale - Spa  | 8,000 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 10   | SJ-2026-0042| 2700    | VAT 25%     | 2,000 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 07   | SJ-2026-0038| 3000    | Sale - Lunch| 5,200 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 07   | SJ-2026-0038| 2700    | VAT 15%     |   780 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 03   | SJ-2026-0031| 4000    | Purchase    | 4,000 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  | Apr 03   | SJ-2026-0031| 2710    | Input VAT   | 1,000 |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  Showing 6 of 12 entries                                   ||
|                  |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |  Export Format:  CSV (Standard Norwegian Accounting Format) ||
|                  |  |                                                            ||
|                  |  |                                     [Export to CSV]         ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Compatibility Notice | Text noting support for Tripletex, Visma, and other Norwegian accounting software |
| Date Range Selector | Start / End date pickers to define export period |
| Export Preview Table | Date, Document Number, Account Code, Description, Amount |
| Transaction Count | "X transactions found" indicator |
| Account Codes | Standard Norwegian chart of accounts (3000 Sales, 2700 Output VAT, 4000 Purchases, 2710 Input VAT) |
| Export Format Label | CSV format indication |
| Export to CSV Button | Generate and download the CSV file |

---

## 10. Register Sale Confirmation (F14 completion)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  SALE REGISTERED                               |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |                                                               |
|                  |  +------------------------------------------------------------+|
| -------------    |  |                                                            ||
|                  |  |                                                            ||
| MANAGEMENT       |  |                  [checkmark icon]                          ||
| # Invoices       |  |                                                            ||
| # Register Sale <|  |              Sale Successfully Registered                   ||
| # Swap Ledger    |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |  |                                                      |  ||
|                  |  |  |  Invoice Number:       SJ-2026-0042                  |  ||
|                  |  |  |  Buyer:                Nordic Wellness AS             |  ||
|                  |  |  |  Amount ex. VAT:       NOK 8,000.00                  |  ||
|                  |  |  |  VAT (25%):            NOK 2,000.00                  |  ||
|                  |  |  |  Total:                NOK 10,000.00                 |  ||
|                  |  |  |                                                      |  ||
|                  |  |  +------------------------------------------------------+  ||
|                  |  |                                                            ||
|                  |  |  Invoice has been sent to: post@nordicwell.no              ||
|                  |  |                                                            ||
|                  |  |  --------------------------------------------------------  ||
|                  |  |                                                            ||
|                  |  |  [View Invoice]  [Register Another Sale]  [Back to Dashboard]||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Success Icon | Large green checkmark icon |
| Success Message | "Sale Successfully Registered" heading |
| Invoice Summary | Invoice Number, Buyer, Amount ex. VAT, VAT, Total |
| Email Confirmation | "Invoice has been sent to: [buyer invoice email]" |
| View Invoice Button | Navigate to the Invoice Detail view for this invoice |
| Register Another Sale Button | Navigate back to the Register Sale form (cleared) |
| Back to Dashboard Button | Navigate to the Company Dashboard |

---

## Component Specifications

### Status Badge Colors

| Status | Text Color | Background Color | Usage |
|--------|-----------|------------------|-------|
| Sent | Blue (#2563eb) | Light blue (#dbeafe) | Invoice sent, awaiting payment |
| Paid | Green (#16a34a) | Light green (#dcfce7) | Invoice has been paid |
| Overdue | Red (#dc2626) | Light red (#fee2e2) | Invoice past due date |
| Draft | Gray (#6b7280) | Light gray (#f3f4f6) | Invoice not yet sent |

### VAT Rate Colors / Labels

| Rate | Label | Color | Usage |
|------|-------|-------|-------|
| 25% | Standard | Blue (#2563eb) | Default rate for most goods/services |
| 15% | Food & Drink | Orange (#f97316) | Food service, beverages |
| 12% | Transport & Hotels | Purple (#a855f7) | Transport, accommodation |
| 0% | Exempt | Gray (#6b7280) | VAT-exempt transactions |

### Credit Balance Display Styles

| Context | Style | Color |
|---------|-------|-------|
| Swap Ledger Balance Card | Large (32px), bold, NOK prefix | Blue (#2563eb) on light blue background |
| Use Points Balance | Large (28px), bold, NOK prefix | Blue (#2563eb) on light blue background |
| Ledger Table - Credit Earned | Regular, green indicator | Green (#16a34a) |
| Ledger Table - Credit Used | Regular, red indicator | Red (#dc2626) |
| Inline Balance | Regular weight, right-aligned | Dark gray (#374151) |

### Invoice Number Format

| Component | Format | Example |
|-----------|--------|---------|
| Prefix | SJ | SJ |
| Year | YYYY | 2026 |
| Sequence | 0001-9999 | 0042 |
| Full Format | SJ-YYYY-NNNN | SJ-2026-0042 |

### Sidebar Navigation - New Items (Owner/Manager)

| Menu Item | Section | Icon | Description |
|-----------|---------|------|-------------|
| Invoices | MANAGEMENT | Document icon | Sent and received invoice archive |
| Register Sale | MANAGEMENT | Plus/cart icon | Create a new sale and invoice |
| Swap Ledger | MANAGEMENT | Ledger/book icon | View point balance and history |

---

**Prepared by:** Rebing Tech
**Project:** SwapJoys Platform
**Module:** VAT / Invoicing
