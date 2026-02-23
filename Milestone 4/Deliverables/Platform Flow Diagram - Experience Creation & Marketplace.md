# SwapJoys Platform - Flow Diagram
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

## Flow Diagram

```mermaid
flowchart TB
    subgraph ENTRY["🚀 ENTRY POINT"]
        A[Owner/Manager Dashboard]
    end
    
    subgraph MY_EXPERIENCES["📋 MY EXPERIENCES - Screen 1"]
        B[Click Experiences in Sidebar]
        C[View My Experiences Grid]
        D[View Stats: Total / Active / Inactive]
        E{Select Action}
    end
    
    subgraph CREATE_EXPERIENCE["➕ CREATE EXPERIENCE - Feature 4"]
        F[Click Create Experience Button]
        G[Display Create Experience Form]
        H[Enter Title]
        I[Enter Description]
        J[Upload Photo]
        K[Set Capacity]
        L[Set Point Cost]
        M[Select Category]
        N[Select City]
        O[Enter Estimated Value - NOK]
        P[Select Welfare Classification]
        Q[Enter Rules - Optional]
        R[Click Publish Experience]
        S{Validate All Fields}
        T[Create Experience Record]
        U[Store Photo to Server]
        V[Set Status: Active]
        W[Show Success Message]
        X[Redirect to My Experiences]
    end
    
    subgraph EDIT_EXPERIENCE["✏️ EDIT EXPERIENCE - Feature 4"]
        Y[Click Edit on Experience]
        Z[Load Experience Data into Form]
        AA[Modify Fields]
        AB[Optionally Upload New Photo]
        AC[Click Save Changes]
        AD{Validate Fields}
        AE[Update Experience in Database]
        AF[Show Success Message]
    end
    
    subgraph DEACTIVATE["🚫 DEACTIVATE / ACTIVATE"]
        AG[Click Deactivate]
        AH[Show Confirmation Modal]
        AI{Confirm?}
        AJ[Set Status: Inactive]
        AK[Hidden from Marketplace]
        AL[Click Activate on Inactive]
        AM[Set Status: Active]
        AN[Visible in Marketplace]
    end
    
    subgraph MARKETPLACE["🏪 MARKETPLACE - Feature 5"]
        AO[Click Marketplace in Sidebar]
        AP[Load Active Experiences from Other Companies]
        AQ[Display Experience Cards Grid]
        AR[Search by Title or Company]
        AS[Filter by Category]
        AT[Filter by City]
        AU[Filters Work Together]
        AV[Click Experience Card]
    end
    
    subgraph EXPERIENCE_DETAIL["📄 EXPERIENCE DETAIL - Feature 5"]
        AW[Load Full Experience Data]
        AX[Display Large Photo]
        AY[Display Title, Description, Badges]
        AZ[Display Point Cost and Capacity]
        BA[Display Estimated Value and Welfare Tag]
        BB[Display Rules and Terms]
        BC[Display Host Company Info]
        BD[Request Experience Button]
        BE[Back to Marketplace]
    end

    %% Main Flow
    A --> B
    B --> C
    C --> D
    D --> E
    
    %% Create Experience Flow
    E -->|Create New| F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    P --> Q
    Q --> R
    R --> S
    S -->|Invalid| G
    S -->|Valid| T
    T --> U
    U --> V
    V --> W
    W --> X
    X --> C
    
    %% Edit Experience Flow
    E -->|Edit| Y
    Y --> Z
    Z --> AA
    AA --> AB
    AB --> AC
    AC --> AD
    AD -->|Invalid| Z
    AD -->|Valid| AE
    AE --> AF
    AF --> C
    
    %% Deactivate Flow
    E -->|Deactivate| AG
    AG --> AH
    AH --> AI
    AI -->|No| C
    AI -->|Yes| AJ
    AJ --> AK
    AK --> C
    
    %% Activate Flow
    E -->|Activate| AL
    AL --> AM
    AM --> AN
    AN --> C
    
    %% Marketplace Flow
    A --> AO
    AO --> AP
    AP --> AQ
    AQ --> AR
    AR --> AS
    AS --> AT
    AT --> AU
    AQ --> AV
    
    %% Experience Detail Flow
    AV --> AW
    AW --> AX
    AX --> AY
    AY --> AZ
    AZ --> BA
    BA --> BB
    BB --> BC
    BC --> BD
    BD -.->|Milestone 5| AQ
    AW --> BE
    BE --> AQ

    %% Styling
    style ENTRY fill:#e0e7ff,stroke:#6366f1,stroke-width:2px
    style MY_EXPERIENCES fill:#fef3c7,stroke:#f59e0b,stroke-width:2px
    style CREATE_EXPERIENCE fill:#d1fae5,stroke:#10b981,stroke-width:2px
    style EDIT_EXPERIENCE fill:#dbeafe,stroke:#3b82f6,stroke-width:2px
    style DEACTIVATE fill:#fee2e2,stroke:#ef4444,stroke-width:2px
    style MARKETPLACE fill:#f3e8ff,stroke:#a855f7,stroke-width:2px
    style EXPERIENCE_DETAIL fill:#fed7aa,stroke:#f97316,stroke-width:2px
```

---

## Flow Summary

| Flow | Description | Actor |
|------|-------------|-------|
| My Experiences | View, manage company's own experiences | Owner/Manager |
| Create Experience | Fill form, upload photo, publish to marketplace | Owner/Manager |
| Edit Experience | Modify existing experience details | Owner/Manager |
| Deactivate/Activate | Toggle experience visibility in marketplace | Owner/Manager |
| Marketplace | Browse, search, filter experiences from other companies | All Roles |
| Experience Detail | View full details of an experience | All Roles |

---

## Key Decision Points

| Decision | Yes Path | No Path |
|----------|----------|---------|
| Validate All Fields (Create) | Create record, store photo, publish | Show errors, stay on form |
| Validate Fields (Edit) | Update record | Show errors, stay on form |
| Confirm Deactivation? | Set inactive, hide from marketplace | Cancel, return to list |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 4 of 8
