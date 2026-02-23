# SwapJoys Platform - User Journey Map
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

## Journey Overview

| Phase | Screens | User Goal | Actor |
|-------|---------|-----------|-------|
| Phase 1 | Create Experience | Create and publish a new experience | Owner/Manager |
| Phase 2 | My Experiences | Manage company's own experiences | Owner/Manager |
| Phase 3 | Browse Marketplace | Discover experiences from other companies | All Roles |
| Phase 4 | Experience Detail | View full details of an experience | All Roles |

---

## Phase 1: Create Experience

**Goal:** Owner/Manager creates a new experience and publishes it to the marketplace

| Step | User Action | System Response |
|------|-------------|-----------------|
| 1.1 | User clicks "Experiences" in sidebar | Navigate to My Experiences page |
| 1.2 | Clicks "+ Create Experience" button | Navigate to Create Experience form |
| 1.3 | Enters experience title | Validate min 3 characters |
| 1.4 | Enters description | Validate min 20 characters |
| 1.5 | Uploads photo | Validate image (JPG/PNG, max 5MB) |
| 1.6 | — | Display image preview |
| 1.7 | Sets capacity (max redemptions) | Validate positive integer |
| 1.8 | Enters rules/terms (optional) | Store text |
| 1.9 | Sets point cost | Validate positive integer |
| 1.10 | Enters estimated value (NOK) | Validate positive number (for tax) |
| 1.11 | Selects welfare classification | Mandatory Yes/No selection |
| 1.12 | Selects category from dropdown | Dining, Wellness, Entertainment, etc. |
| 1.13 | Selects city from dropdown | Norwegian cities list |
| 1.14 | Clicks "Publish Experience" | Validate all required fields |
| 1.15 | — | Create experience record in database |
| 1.16 | — | Store photo to server |
| 1.17 | — | Set status to "Active" |
| 1.18 | — | Show success message |
| 1.19 | — | Redirect to My Experiences list |

**Success Criteria:**
- Experience record created with all fields
- Photo uploaded and stored
- Experience visible in marketplace to other companies
- Estimated value and welfare tag stored for tax documentation

**Error Handling:**

| Error | Message | Action |
|-------|---------|--------|
| Missing required field | "Please fill in all required fields" | Highlight empty fields |
| Title too short | "Title must be at least 3 characters" | Highlight field |
| Description too short | "Description must be at least 20 characters" | Highlight field |
| Invalid image format | "Only JPG and PNG images are allowed" | Show error |
| Image too large | "Image must be less than 5MB" | Show error |
| No photo uploaded | "Please upload a photo for your experience" | Highlight upload area |
| No welfare tag selected | "Welfare classification is required" | Highlight field |
| Invalid point value | "Point cost must be a positive number" | Highlight field |

---

## Phase 2: My Experiences

**Goal:** Owner/Manager views and manages their company's experiences

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.1 | User clicks "Experiences" in sidebar | Navigate to My Experiences page |
| 2.2 | — | Load all company experiences |
| 2.3 | — | Display experience cards in grid layout |
| 2.4 | User views stats cards | Show: Total, Active, Inactive counts |
| 2.5 | User clicks an experience card | Navigate to experience detail (owner view) |
| 2.6 | User clicks "Edit" on an experience | Navigate to Edit Experience form |
| 2.7 | User clicks "Deactivate" on an experience | Show confirmation modal |
| 2.8 | Confirms deactivation | Set experience status to "Inactive" |
| 2.9 | — | Experience hidden from marketplace |
| 2.10 | User clicks "Activate" on inactive experience | Set status to "Active" |
| 2.11 | — | Experience visible in marketplace again |

### Edit Experience Flow

| Step | User Action | System Response |
|------|-------------|-----------------|
| 2.E1 | User clicks "Edit" on experience | Load experience data into form |
| 2.E2 | Modifies any field(s) | Real-time validation |
| 2.E3 | Optionally uploads new photo | Replace existing photo preview |
| 2.E4 | Clicks "Save Changes" | Validate all fields |
| 2.E5 | — | Update experience in database |
| 2.E6 | — | Show success message |
| 2.E7 | — | Redirect to My Experiences |

**Success Criteria:**
- All company experiences displayed with status
- Edit updates reflected immediately
- Deactivated experiences hidden from marketplace
- Reactivated experiences visible again

---

## Phase 3: Browse Marketplace

**Goal:** Any user browses available experiences from other companies

| Step | User Action | System Response |
|------|-------------|-----------------|
| 3.1 | User clicks "Marketplace" in sidebar | Navigate to Marketplace page |
| 3.2 | — | Load all active experiences from other companies |
| 3.3 | — | Display experiences in card grid layout |
| 3.4 | User sees experience cards | Each card shows: Photo, Title, Company, Points, City, Category |
| 3.5 | User selects category filter | Filter experiences by category |
| 3.6 | User selects city filter | Filter experiences by city |
| 3.7 | User applies both filters together | Show experiences matching both filters |
| 3.8 | User uses search box | Search by experience title or company name |
| 3.9 | User clicks an experience card | Navigate to Experience Detail page |

**Filter Options:**

| Filter | Options |
|--------|---------|
| Category | All, Dining, Wellness, Entertainment, Activities, Culture, Travel, Other |
| City | All, Oslo, Bergen, Trondheim, Stavanger, Tromsø, Kristiansand, Drammen, Fredrikstad, Other |

**Success Criteria:**
- Only active experiences from other companies displayed
- Company's own experiences NOT shown in marketplace
- Filters work individually and in combination
- Search works on title and company name

---

## Phase 4: Experience Detail

**Goal:** User views full details of an experience before requesting/booking

| Step | User Action | System Response |
|------|-------------|-----------------|
| 4.1 | User clicks experience card in marketplace | Navigate to Experience Detail page |
| 4.2 | — | Load full experience data |
| 4.3 | User sees experience photo | Display large photo |
| 4.4 | User sees experience title | Display title prominently |
| 4.5 | User sees description | Display full description |
| 4.6 | User sees point cost | Display points required |
| 4.7 | User sees capacity | Display remaining/total capacity |
| 4.8 | User sees rules/terms | Display experience rules |
| 4.9 | User sees category badge | Display category tag |
| 4.10 | User sees city location | Display city name |
| 4.11 | User sees host company info | Display company name and details |
| 4.12 | User sees estimated value (NOK) | Display market value |
| 4.13 | User sees welfare classification | Display Yes/No badge |
| 4.14 | User clicks "Request Experience" button | (Milestone 5 functionality) |
| 4.15 | User clicks "← Back to Marketplace" | Return to marketplace |

**Note:** The "Request Experience" button will be visible but the booking workflow is implemented in Milestone 5.

**Success Criteria:**
- All experience details displayed clearly
- Host company information visible
- Tax-related fields (estimated value, welfare tag) visible
- Back navigation to marketplace works

---

## Screen Summary

| # | Screen Name | Entry Point | Exit Point |
|---|-------------|-------------|------------|
| 1 | Create Experience | "Create Experience" button | Submit → My Experiences |
| 2 | My Experiences | Sidebar "Experiences" | Click card → Detail |
| 3 | Edit Experience | "Edit" button on experience | Save → My Experiences |
| 4 | Marketplace | Sidebar "Marketplace" | Click card → Detail |
| 5 | Experience Detail | Click card in marketplace | Back → Marketplace |
| 6 | Experience Detail (Owner) | Click card in My Experiences | Back → My Experiences |
| 7 | Empty State | No experiences created yet | CTA → Create Experience |

---

## Validation Rules Summary

| Field | Rules |
|-------|-------|
| Title | Required, Min 3 characters, Max 150 characters |
| Description | Required, Min 20 characters, Max 2000 characters |
| Photo | Required, JPG or PNG, Max 5MB |
| Capacity | Required, Positive integer, Min 1 |
| Rules/Terms | Optional, Max 1000 characters |
| Point Cost | Required, Positive integer, Min 1 |
| Estimated Value (NOK) | Required, Positive number |
| Welfare Classification | Required, Must select Yes or No |
| Category | Required, Select from list |
| City | Required, Select from list |

---

## Category Options

| Category | Icon |
|----------|------|
| Dining | 🍽️ |
| Wellness | 💆 |
| Entertainment | 🎭 |
| Activities | 🏃 |
| Culture | 🎨 |
| Travel | ✈️ |
| Other | 📦 |

---

## Experience Status

| Status | Description | Marketplace Visibility |
|--------|-------------|----------------------|
| Active | Published and available | ✅ Visible |
| Inactive | Deactivated by owner | ❌ Hidden |

---

## Role-Based Access

| Action | Owner | Manager | Employee |
|--------|:-----:|:-------:|:--------:|
| Create Experience | ✅ | ✅ | ❌ |
| Edit Experience | ✅ | ✅ | ❌ |
| Deactivate/Activate | ✅ | ✅ | ❌ |
| View My Experiences | ✅ | ✅ | ❌ |
| Browse Marketplace | ✅ | ✅ | ✅ |
| View Experience Detail | ✅ | ✅ | ✅ |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 4 of 8
