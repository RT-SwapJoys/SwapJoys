# SwapJoys Platform - Flow Diagram
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

## Flow Diagram

```mermaid
flowchart TB
    subgraph ENTRY["🚀 ENTRY POINTS"]
        A1[Company Owner/Manager]
        A2[SwapJoys Admin]
    end

    subgraph BALANCE_DASHBOARD["💰 POINTS & BALANCE DASHBOARD - Feature 9"]
        B1[Click Points & Balance in Sidebar]
        B2[Load Company Points Data]
        B3[Calculate Balance:<br/>Earned − Spent = Current]
        B4[Display Balance Summary Cards]
        B5[Card: Current Balance<br/>Large prominent number]
        B6[Card: Points Earned<br/>Total credits]
        B7[Card: Points Spent<br/>Total debits]
        B8[Card: Pending Bookings<br/>Reserved points]
        B9[Display Recent Transactions<br/>Last 5-10 entries]
        B10[Each Entry: Date, Type,<br/>Experience, Points +/-, Party]
        B11{Select Action}
    end

    subgraph TRANSACTION_HISTORY["📜 TRANSACTION HISTORY - Feature 8"]
        C1[Click View All Transactions]
        C2[Load All Transactions<br/>from Points Ledger]
        C3[Display Transaction Table<br/>Newest First]
        C4[Columns: Date, Type, Description,<br/>Points +/-, Balance After, Party]
        C5[Filter by Type Dropdown]
        C6[Filter by Date Range]
        C7[Search by Experience or Company]
        C8[Filters Work Together]
        C9[Pagination: 20 per page]
        C10{Click Transaction Row}
    end

    subgraph TRANSACTION_DETAIL["🔍 TRANSACTION DETAIL - Feature 8"]
        D1[Load Full Transaction Data]
        D2[Display: Transaction ID]
        D3[Display: Date/Time]
        D4[Display: Type with Icon]
        D5[Display: Experience Name]
        D6[Display: Points Amount +/-]
        D7[Display: Balance Before]
        D8[Display: Balance After]
        D9[Display: Other Party]
        D10[Display: Notes/Reason]
        D11[Back to Transaction History]
    end

    subgraph POINTS_DISPLAY["🏷️ POINTS ACROSS PLATFORM - Feature 8"]
        E1[Marketplace Experience Cards:<br/>Show Point Cost]
        E2[Experience Detail Page:<br/>Show Point Cost Prominently]
        E3[Booking Request Form:<br/>Show Balance vs Cost]
        E4{Balance ≥ Cost?}
        E5[Show Sufficient Indicator ✅]
        E6[Show Insufficient Warning ⚠️]
        E7[Dashboard Header:<br/>Show Current Balance]
        E8[My Bookings:<br/>Show Points per Booking]
    end

    subgraph ADMIN_ADJUSTMENT["⚙️ ADMIN POINT ADJUSTMENTS - Feature 10"]
        F1[Admin Clicks Point Adjustments]
        F2[Display Company List<br/>with Current Balances]
        F3[Search Company by Name]
        F4[Select Company]
        F5[Show Company Current Balance]
        F6[Click Adjust Points]
        F7[Open Adjustment Form]
        F8[Select Type: Add / Remove]
        F9[Enter Point Amount]
        F10[Enter Reason - Mandatory<br/>Min 10 characters]
        F11[Click Apply Adjustment]
        F12[Show Confirmation Dialog]
        F13{Confirm?}
        F14{Validate Fields}
        F15[Show Validation Errors]
    end

    subgraph ADMIN_PROCESS["✅ PROCESS ADJUSTMENT"]
        G1[Update Company Points Balance]
        G2[Create Points Ledger Entry<br/>Append-Only / Immutable]
        G3[Create Admin Audit Log Entry]
        G4[Show Success Message<br/>with New Balance]
        G5[Return to Company List<br/>with Updated Balance]
    end

    subgraph ADMIN_HISTORY["📋 ADJUSTMENT HISTORY - Feature 10"]
        H1[Click Adjustment History Tab]
        H2[Load All Admin Adjustments]
        H3[Display Table: Date, Admin,<br/>Company, Type, Amount, Reason]
        H4[Filter by Company]
        H5[Filter by Date Range]
        H6[Filter by Type: Add / Remove]
        H7{Click Adjustment Row}
        H8[Display Full Detail:<br/>ID, Admin, Company, Type,<br/>Amount, Balance Before/After,<br/>Reason, Timestamp]
        H9[Back to Adjustment History]
    end

    subgraph TRANSACTION_TYPES["📊 TRANSACTION TYPES"]
        T1["🎁 Welcome Bonus: +50"]
        T2["📤 Booking Deduction: −X"]
        T3["📥 Redemption Credit: +X"]
        T4["⚙️ Admin Add: +X"]
        T5["⚙️ Admin Remove: −X"]
    end

    %% Company User Flows
    A1 --> B1
    B1 --> B2
    B2 --> B3
    B3 --> B4
    B4 --> B5
    B4 --> B6
    B4 --> B7
    B4 --> B8
    B4 --> B9
    B9 --> B10
    B10 --> B11

    %% To Transaction History
    B11 -->|View All| C1
    C1 --> C2
    C2 --> C3
    C3 --> C4
    C4 --> C5
    C5 --> C6
    C6 --> C7
    C7 --> C8
    C8 --> C9
    C9 --> C10

    %% Transaction Detail
    C10 -->|Click Row| D1
    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> D5
    D5 --> D6
    D6 --> D7
    D7 --> D8
    D8 --> D9
    D9 --> D10
    D10 --> D11
    D11 --> C3

    %% Points Display
    A1 --> E1
    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 -->|Yes| E5
    E4 -->|No| E6
    A1 --> E7
    A1 --> E8

    %% Admin Flows
    A2 --> F1
    F1 --> F2
    F2 --> F3
    F3 --> F4
    F4 --> F5
    F5 --> F6
    F6 --> F7
    F7 --> F8
    F8 --> F9
    F9 --> F10
    F10 --> F11
    F11 --> F12
    F12 --> F13
    F13 -->|No| F7
    F13 -->|Yes| F14
    F14 -->|Invalid| F15
    F15 --> F7
    F14 -->|Valid| G1
    G1 --> G2
    G2 --> G3
    G3 --> G4
    G4 --> G5
    G5 --> F2

    %% Admin History
    A2 --> H1
    H1 --> H2
    H2 --> H3
    H3 --> H4
    H4 --> H5
    H5 --> H6
    H6 --> H7
    H7 -->|Click Row| H8
    H8 --> H9
    H9 --> H3

    %% Transaction Types (dotted connections)
    T1 -.-> C2
    T2 -.-> C2
    T3 -.-> C2
    T4 -.-> C2
    T5 -.-> C2

    %% Styling
    style ENTRY fill:#e0e7ff,stroke:#6366f1,stroke-width:2px
    style BALANCE_DASHBOARD fill:#fef3c7,stroke:#f59e0b,stroke-width:2px
    style TRANSACTION_HISTORY fill:#dbeafe,stroke:#3b82f6,stroke-width:2px
    style TRANSACTION_DETAIL fill:#f0fdf4,stroke:#22c55e,stroke-width:2px
    style POINTS_DISPLAY fill:#fce7f3,stroke:#ec4899,stroke-width:2px
    style ADMIN_ADJUSTMENT fill:#f3e8ff,stroke:#a855f7,stroke-width:2px
    style ADMIN_PROCESS fill:#d1fae5,stroke:#10b981,stroke-width:2px
    style ADMIN_HISTORY fill:#fed7aa,stroke:#f97316,stroke-width:2px
    style TRANSACTION_TYPES fill:#f5f5f5,stroke:#9ca3af,stroke-width:1px
```

---

## Flow Summary

| Flow | Description | Actor |
|------|-------------|-------|
| Points & Balance Dashboard | View balance summary, earned/spent totals, recent transactions | Company Owner/Manager |
| Transaction History | Browse, filter, and search all point movements | Company Owner/Manager |
| Transaction Detail | View full details of a single transaction | Company Owner/Manager |
| Points Display | See point values on experience cards, detail pages, and booking forms | All Company Roles |
| Admin Point Adjustments | Select company, add/remove points with mandatory reason | SwapJoys Admin |
| Admin Adjustment Processing | Update balance, create ledger entry, log audit trail | System |
| Admin Adjustment History | View, filter, and inspect all past admin adjustments | SwapJoys Admin |

---

## Key Decision Points

| Decision | Yes Path | No Path |
|----------|----------|---------|
| Balance ≥ Experience Cost? | Show sufficient indicator, allow booking | Show insufficient warning, block booking |
| Admin Confirms Adjustment? | Validate and process | Return to form |
| Validate Adjustment Fields? | Update balance, create ledger + audit entries | Show validation errors |

---

## Points Ledger Architecture

```
APPEND-ONLY IMMUTABLE LEDGER

Each entry records:
├── Transaction ID (unique)
├── Company ID
├── Type (welcome_bonus / booking_deduction / redemption_credit / admin_adjustment)
├── Points (positive for credit, negative for debit)
├── Balance After (calculated running balance)
├── Reference ID (booking_id, ticket_id, or adjustment_id)
├── Description
├── Created At (timestamp)
└── Cannot be edited or deleted
```

---

## Balance Calculation Flow

```
CURRENT BALANCE = Sum of all ledger entries for company

Entry 1: Welcome Bonus         +50    Balance: 50
Entry 2: Booking Approved       -30    Balance: 20
Entry 3: Ticket Redeemed        +25    Balance: 45
Entry 4: Admin Adjustment       +100   Balance: 145
Entry 5: Booking Approved       -40    Balance: 105
...
```

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 6 of 8
