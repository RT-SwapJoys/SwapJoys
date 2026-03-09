# SwapJoys Platform - Flow Diagram
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

## Flow Diagram

```mermaid
flowchart TB
    subgraph ENTRY["🚀 ENTRY POINTS"]
        A1[Requesting Company<br/>Owner/Manager]
        A2[Host Company<br/>Owner/Manager]
        A3[Assigned Employee]
    end

    subgraph REQUEST_FLOW["📩 REQUEST EXPERIENCE - Feature 6"]
        B1[View Experience Detail in Marketplace]
        B2[Click Request Experience]
        B3{Balance Check<br/>Points ≥ Cost?}
        B4[Show Insufficient Points Warning]
        B5[Open Request Form]
        B6[Select Employee from Dropdown]
        B7[Select Preferred Date]
        B8[Enter Message to Host - Optional]
        B9[Click Submit Request]
        B10{Validate Fields}
        B11[Create Booking Record<br/>Status: PENDING]
        B12[Send Email to Host Company]
        B13[Show Success Message]
        B14[Redirect to My Bookings]
    end

    subgraph INCOMING_REQUESTS["📥 INCOMING REQUESTS - Feature 6"]
        C1[Host clicks My Bookings]
        C2[Select Incoming Requests Tab]
        C3[View Request List with Stats]
        C4[Click Request to View Details]
        C5[View Full Request Info:<br/>Company, Employee, Date, Message]
        C6{Host Decision}
    end

    subgraph APPROVE_FLOW["✅ APPROVE REQUEST"]
        D1[Click Approve]
        D2[Show Confirmation Dialog]
        D3[Confirm Approval]
        D4[Update Status: CONFIRMED]
        D5[Deduct Points from<br/>Requesting Company]
        D6[Generate QR Code<br/>Unique Ticket UUID]
        D7[Generate Backup Code<br/>6-char Alphanumeric]
        D8[Create Ticket Record]
        D9[Create Transaction Log Entry]
        D10[Send Approval Email<br/>to Requesting Company]
        D11[Show Success: Ticket Created]
    end

    subgraph REJECT_FLOW["❌ REJECT REQUEST"]
        E1[Click Reject]
        E2[Open Rejection Modal]
        E3[Enter Reason - Required]
        E4{Reason Valid?<br/>Min 10 chars}
        E5[Update Status: REJECTED]
        E6[Send Rejection Email<br/>with Reason]
        E7[Show Confirmation]
    end

    subgraph MY_BOOKINGS["📋 MY BOOKINGS - Outgoing"]
        F1[User clicks My Bookings]
        F2[View Outgoing Bookings Tab]
        F3[View Stats: Total / Pending /<br/>Confirmed / Used / Rejected]
        F4[Filter by Status]
        F5{Click Booking}
        F6[Pending: Show Request Details]
        F7[Confirmed: Navigate to Ticket View]
        F8[Rejected: Show Reason]
        F9[Used: Show Redemption Details]
    end

    subgraph TICKET_VIEW["🎫 TICKET & QR CODE - Feature 7"]
        G1[Open Ticket View]
        G2[Display Ticket Info:<br/>Experience, Host, Employee, Date]
        G3[Display QR Code - Large Scannable]
        G4[Display Backup Code Below QR]
        G5[Click Show to Host Button]
        G6[Enter Full-Screen QR Mode<br/>Dark Background, Max Size]
        G7[Display Backup Code Prominently]
        G8[Tap Anywhere to Exit]
    end

    subgraph SCANNER["📷 QR SCANNER & REDEMPTION - Feature 7"]
        H1[Host navigates to Scan Ticket]
        H2{Camera Permission?}
        H3[Open Camera Scanner]
        H4[Show Manual Entry Option]
        H5[Scan QR Code]
        H6[Enter 6-Char Code Manually]
        H7{Validate Code}
        H8[Invalid/Used/Expired/Wrong Host]
        H9[Show Error Message]
        H10[Display Ticket Summary<br/>for Confirmation]
        H11[Click Confirm Redemption]
        H12[Update Ticket Status: USED]
        H13[Credit Points to Host Company]
        H14[Create Transaction Log<br/>Points Credit]
        H15[Create Usage Documentation<br/>Employee, Experience, Date,<br/>Value, Company, Welfare Tag]
        H16[Show Success Screen<br/>+X Points Credited]
        H17[Send Redemption Email<br/>to Requesting Company]
    end

    subgraph STATUS_TRACKING["🏷️ STATUS TRACKING - Feature 13"]
        S1[Status: PENDING<br/>🟡 Orange Badge]
        S2[Status: CONFIRMED<br/>🔵 Blue Badge]
        S3[Status: USED<br/>🟢 Green Badge]
        S4[Status: REJECTED<br/>🔴 Red Badge]
    end

    %% Request Flow
    A1 --> B1
    B1 --> B2
    B2 --> B3
    B3 -->|No| B4
    B3 -->|Yes| B5
    B5 --> B6
    B6 --> B7
    B7 --> B8
    B8 --> B9
    B9 --> B10
    B10 -->|Invalid| B5
    B10 -->|Valid| B11
    B11 --> S1
    B11 --> B12
    B12 --> B13
    B13 --> B14

    %% Incoming Requests Flow
    A2 --> C1
    C1 --> C2
    C2 --> C3
    C3 --> C4
    C4 --> C5
    C5 --> C6

    %% Approve
    C6 -->|Approve| D1
    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> S2
    D4 --> D5
    D5 --> D6
    D6 --> D7
    D7 --> D8
    D8 --> D9
    D9 --> D10
    D10 --> D11

    %% Reject
    C6 -->|Reject| E1
    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 -->|No| E2
    E4 -->|Yes| E5
    E5 --> S4
    E5 --> E6
    E6 --> E7

    %% My Bookings
    A1 --> F1
    F1 --> F2
    F2 --> F3
    F3 --> F4
    F4 --> F5
    F5 -->|Pending| F6
    F5 -->|Confirmed| F7
    F5 -->|Rejected| F8
    F5 -->|Used| F9

    %% Ticket View
    F7 --> G1
    A3 --> G1
    G1 --> G2
    G2 --> G3
    G3 --> G4
    G4 --> G5
    G5 --> G6
    G6 --> G7
    G7 --> G8

    %% Scanner
    A2 --> H1
    H1 --> H2
    H2 -->|Granted| H3
    H2 -->|Denied| H4
    H3 --> H5
    H4 --> H6
    H5 --> H7
    H6 --> H7
    H7 -->|Invalid| H8
    H8 --> H9
    H9 --> H3
    H7 -->|Valid| H10
    H10 --> H11
    H11 --> H12
    H12 --> S3
    H12 --> H13
    H13 --> H14
    H14 --> H15
    H15 --> H16
    H16 --> H17

    %% Status Transitions (dotted)
    S1 -.->|Host Approves| S2
    S1 -.->|Host Rejects| S4
    S2 -.->|QR Scanned / Code Entered| S3

    %% Styling
    style ENTRY fill:#e0e7ff,stroke:#6366f1,stroke-width:2px
    style REQUEST_FLOW fill:#fef3c7,stroke:#f59e0b,stroke-width:2px
    style INCOMING_REQUESTS fill:#fce7f3,stroke:#ec4899,stroke-width:2px
    style APPROVE_FLOW fill:#d1fae5,stroke:#10b981,stroke-width:2px
    style REJECT_FLOW fill:#fee2e2,stroke:#ef4444,stroke-width:2px
    style MY_BOOKINGS fill:#dbeafe,stroke:#3b82f6,stroke-width:2px
    style TICKET_VIEW fill:#f3e8ff,stroke:#a855f7,stroke-width:2px
    style SCANNER fill:#fed7aa,stroke:#f97316,stroke-width:2px
    style STATUS_TRACKING fill:#f0fdf4,stroke:#22c55e,stroke-width:2px
```

---

## Flow Summary

| Flow | Description | Actor |
|------|-------------|-------|
| Request Experience | Select employee, date, submit request | Requesting Company Owner/Manager |
| Incoming Requests | View, approve, or reject booking requests | Host Company Owner/Manager |
| Approve Request | Deduct points, generate QR + backup code, create ticket | Host Company Owner/Manager |
| Reject Request | Decline with reason, notify requesting company | Host Company Owner/Manager |
| My Bookings | View all outgoing bookings with status | Requesting Company (All Roles) |
| Ticket & QR Display | View ticket, show QR in full-screen to host | Assigned Employee |
| QR Scanner | Scan QR or enter manual code, confirm redemption | Host Company Owner/Manager |
| Status Tracking | Visual status badges across all views | All Roles |

---

## Key Decision Points

| Decision | Yes Path | No Path |
|----------|----------|---------|
| Balance ≥ Cost? | Open request form | Show insufficient points warning |
| Validate Request Fields? | Create booking, send notification | Show errors, stay on form |
| Host Approves? | Deduct points, create ticket + QR | — |
| Host Rejects? | Update status, notify with reason | — |
| Rejection Reason Valid? | Process rejection | Stay on modal |
| Camera Permission Granted? | Open QR scanner | Show manual code entry |
| Code Valid? | Show ticket summary for confirmation | Show error, retry |

---

## Points Settlement Flow

```
REQUEST SUBMITTED
    └── Points checked but NOT deducted
    
HOST APPROVES
    └── Points DEDUCTED from requesting company
    └── Ticket + QR code created
    
TICKET REDEEMED (QR Scanned)
    └── Points CREDITED to host company
    └── Transaction logged
    └── Usage documented for tax
```

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 5 of 8
