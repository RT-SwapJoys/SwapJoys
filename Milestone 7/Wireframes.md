# SwapJoys Platform - Wireframes
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

## Screen Overview

| # | Screen | Description | Actor |
|---|--------|-------------|-------|
| 1 | Company Dashboard (Owner/Manager) | Company stats, recent bookings, quick actions | Owner/Manager |
| 2 | Company Dashboard (Employee) | Personal stats, upcoming bookings, recent usage | Employee |
| 3 | Admin Dashboard Overview | Platform metrics, recent activity | SwapJoys Admin |
| 4 | Admin - Company List | All companies with search and status | SwapJoys Admin |
| 5 | Admin - Company Detail | Company info, stats, employees, status control | SwapJoys Admin |
| 6 | Admin - Experience List | All experiences with NOK value, welfare tag, filters | SwapJoys Admin |
| 7 | Admin - Experience Detail | Full experience info including NOK and welfare | SwapJoys Admin |
| 8 | Admin - Transaction Log | All transactions with filters and CSV export | SwapJoys Admin |
| 9 | Admin - Redemption Log | All redemptions with NOK value and welfare tag | SwapJoys Admin |
| 10 | Admin - Company Activity | Per-company activity log | SwapJoys Admin |
| 11 | Admin - Employee Activity | Per-employee activity log | SwapJoys Admin |
| 12 | Experience Detail (NOK + Welfare) | NOK value and welfare badge on experience page | All Roles |
| 13 | Company - Usage Documentation | Employee usage logs for tax reporting | Owner/Manager |

---

## 1. Company Dashboard (Owner/Manager View)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  COMPANY DASHBOARD                             |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Welcome back, Ola                                            |
|                  |  TechCorp AS                                                   |
| -------------    |                                                                |
|                  |  +-------------+  +-------------+  +-------------+  +----------+
| MAIN MENU        |  | 1,250        |  | 12           |  | 4            |  | 28      |
|                  |  |              |  |              |  |              |  |         |
| # Dashboard  <   |  | Points       |  | Total        |  | Active       |  | Total   |
| # Experiences    |  | Balance      |  | Employees    |  | Experiences  |  | Bookings|
| # My Bookings    |  |              |  |              |  |              |  |         |
| # Points &       |  +-------------+  +-------------+  +-------------+  +----------+
|   Balance        |                                                                |
| MANAGEMENT       |  +---------------------------------------+  +----------------+ |
| # Employees      |  | Points Activity (Last 6 Months)       |  | Booking Status | |
| # My Experiences |  |                                       |  |                | |
| # Tax Reports    |  |  400|     ██                           |  |   +--------+  | |
| # Redeem Ticket  |  |  300|  ██ ██ ██                        |  |  / Used 18 \  | |
| # Settings       |  |  200|████████████                      |  | | Conf.  4  | | |
|                  |  |  100|████████████                      |  |  \ Pend. 3 /  | |
|                  |  |    0+--+--+--+--+--+--                 |  |   +--------+  | |
|                  |  |     Nov Dec Jan Feb Mar Apr            |  | Rejected: 3  | |
|                  |  |  [Earned] [Spent]                      |  |                | |
|                  |  +---------------------------------------+  +----------------+ |
|                  |                                                                |
|                  |  +---------------------------+  +---------------------------+  |
|                  |  | Quick Actions             |  | Recent Bookings            |  |
|                  |  |                           |  |                           |  |
|                  |  | [+ Create Experience]     |  | Apr 7  Spa Day     Pending|  |
|                  |  | [+ Add Employee]          |  | Apr 6  Team Lunch  Approved|  |
|                  |  | [View Points & Balance]   |  | Apr 5  Gym Session Confirmed|  |
|                  |  | [Redeem Ticket]           |  | Apr 3  Cooking Cls Used   |  |
|                  |  |                           |  | Apr 1  Movie Night Rejected|  |
|                  |  +---------------------------+  +---------------------------+  |
|                  |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  | Recent Redemptions                                        ||
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | DATE      | EMPLOYEE       | EXPERIENCE      | NOK VALUE  ||
|                  |  | ----------+----------------+-----------------+----------- ||
|                  |  | Apr 7     | Ola Nordmann   | Spa Day Package | 1,500      ||
|                  |  | Apr 5     | Kari Hansen    | Team Lunch      | 800        ||
|                  |  | Apr 3     | Per Olsen      | Gym Session     | 600        ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Welcome Message | "Welcome back, [Name]" with company name |
| Points Balance Card | Current company points balance, clickable → Points & Balance |
| Total Employees Card | Employee count, clickable → Employees page |
| Active Experiences Card | Published experience count, clickable → My Experiences |
| Total Bookings Card | Total bookings count, clickable → My Bookings |
| Points Activity Chart | Bar chart: Points Earned vs Spent per month (last 6 months) |
| Booking Status Chart | Doughnut chart: Used, Confirmed, Pending, Rejected breakdown |
| Quick Actions | Buttons for Create Experience, Add Employee, View Points, Redeem Ticket |
| Recent Bookings | Last 5 bookings (incoming + outgoing) with status badges |
| Recent Redemptions | Last 5 completed redemptions with employee, experience, NOK value |

---

## 2. Company Dashboard (Employee View)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  MY DASHBOARD                                  |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Welcome back, Per                                            |
|                  |  TechCorp AS                                                   |
| -------------    |                                                                |
|                  |  +------------------+  +------------------+  +------------------+
| MAIN MENU        |  | 45                |  | 3                 |  | 5                |
|                  |  |                  |  |                  |  |                  |
| # Dashboard  <   |  | Available        |  | My Active        |  | Experiences      |
| # Experiences    |  | Experiences      |  | Bookings         |  | Used             |
| # My Bookings    |  |                  |  |                  |  |                  |
|                  |  +------------------+  +------------------+  +------------------+
| -------------    |                                                                |
|                  |  +---------------------------+  +---------------------------+  |
| # Redeem Ticket  |  | My Experiences (6 Months) |  | Experiences by Category   |  |
|                  |  |                           |  |                           |  |
|                  |  |   2|        ██             |  |      +----------+        |  |
|                  |  |   1|  ██ ██    ██          |  |     / Wellness  \       |  |
|                  |  |   0+--+--+--+--+--+--     |  |    | Dining Fit |       |  |
|                  |  |    Nov Dec Jan Mar Apr     |  |     \ Entertain /       |  |
|                  |  |                           |  |      +----------+        |  |
|                  |  +---------------------------+  +---------------------------+  |
|                  |                                                                |
|                  |  +---------------------------+  +---------------------------+  |
|                  |  | Quick Actions             |  | My Upcoming Bookings      |  |
|                  |  |                           |  |                           |  |
|                  |  | [Browse Experiences]      |  | Apr 10  Spa Day   Confirmed|  |
|                  |  | [View My Bookings]        |  | Apr 15  Team Lunch Pending|  |
|                  |  |                           |  |                           |  |
|                  |  +---------------------------+  +---------------------------+  |
|                  |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  | Recently Used Experiences                                 ||
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | DATE      | EXPERIENCE           | HOST COMPANY           ||
|                  |  | ----------+----------------------+----------------------- ||
|                  |  | Apr 3     | Gym Session Pass     | FitNord AS             ||
|                  |  | Mar 20    | Cooking Class        | TechCorp AS            ||
|                  |  | Mar 10    | Movie Night          | Bergen Events AS       ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Welcome Message | "Welcome back, [Name]" with company name |
| Available Experiences Card | Count of browsable experiences, clickable → Experiences |
| My Active Bookings Card | Count of active bookings, clickable → My Bookings |
| Experiences Used Card | Total experiences redeemed, clickable → My Bookings |
| My Experiences Chart | Bar chart: Experiences used per month (last 6 months) |
| Category Chart | Doughnut chart: Wellness, Dining, Fitness, Entertainment breakdown |
| Quick Actions | Browse Experiences, View My Bookings |
| My Upcoming Bookings | Confirmed tickets not yet used, with date and status |
| Recently Used Experiences | Last 5 redeemed experiences with date, name, host |

---

## 3. Admin Dashboard Overview

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                 ADMIN DASHBOARD                               |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Dashboard                                                    |
|    ADMIN         |  Platform overview and key metrics                             |
|                  |                                                                |
| -------------    |  +-------------+  +-------------+  +-------------+  +----------+
|                  |  | 24           |  | 186          |  | 45           |  | 312     |
| ADMIN MENU       |  |              |  |              |  |              |  |         |
|                  |  | Total        |  | Total        |  | Active       |  | Total   |
| # Dashboard  <   |  | Companies    |  | Employees    |  | Experiences  |  | Redemp. |
| # Companies      |  |              |  |              |  |              |  |         |
| # Experiences    |  +-------------+  +-------------+  +-------------+  +----------+
| # Usage Logs     |                                                                |
| # Point          |  +-------------+                                               |
|   Adjustments    |  | 8,450        |                                               |
| # Settings       |  |              |                                               |
|                  |  | Points in    |                                               |
|                  |  | Circulation  |                                               |
|                  |  +-------------+                                               |
|                  |                                                                |
|                  |  +---------------------+ +------------------+ +-------------+  |
|                  |  | Platform Growth      | | Monthly Redempt. | | Points by   |  |
|                  |  |                     | |                  | | Company     |  |
|                  |  |     /--*            | |  80|     ##      | |  +-------+  |  |
|                  |  |   *-    \--*        | |  60|  ## ##      | | / Tech   \  |  |
|                  |  |  /         \        | |  40|########     | ||Nord Food|| |  |
|                  |  | *           *       | |  20|########     | | \ Others /  |  |
|                  |  | Nov  Jan  Mar  Apr  | |   0+--+--+--+-- | |  +-------+  |  |
|                  |  | [Companies] [Empl.] | |                  | |             |  |
|                  |  +---------------------+ +------------------+ +-------------+  |
|                  |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  | Recent Activity                                           ||
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | DATE      | EVENT                        | COMPANY         ||
|                  |  | ----------+------------------------------+--------------- ||
|                  |  | Apr 7     | New company registered       | TechCorp AS    ||
|                  |  | 14:30     |                              |                ||
|                  |  | ----------+------------------------------+--------------- ||
|                  |  | Apr 7     | Experience redeemed          | Nordic Well AS ||
|                  |  | 11:15     | Spa Day Package              |                ||
|                  |  | ----------+------------------------------+--------------- ||
|                  |  | Apr 6     | Booking approved             | FoodCorp AS    ||
|                  |  | 16:45     | Team Lunch Experience        |                ||
|                  |  | ----------+------------------------------+--------------- ||
|                  |  | Apr 6     | Admin adjusted points        | FitNord AS     ||
|                  |  | 10:00     | +50 points                   |                ||
|                  |  | ----------+------------------------------+--------------- ||
|                  |  | Apr 5     | New employee added           | TechCorp AS    ||
|                  |  | 09:30     | Kari Hansen                  |                ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Total Companies Card | Count of all registered companies |
| Total Employees Card | Count of all employees across platform |
| Active Experiences Card | Count of published experiences |
| Total Redemptions Card | Count of completed redemptions |
| Points in Circulation Card | Sum of all company point balances |
| Platform Growth Chart | Line chart: Companies + Employees registered per month (6 months) |
| Monthly Redemptions Chart | Bar chart: Redemption count per month (6 months) |
| Points by Company Chart | Doughnut chart: Points distribution across top companies |
| Recent Activity | Last 10 platform events with timestamp, event, company |

---

## 4. Admin - Company List

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  COMPANIES                                     |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Companies                                 [24 total]         |
|    ADMIN         |  Manage all registered companies                               |
|                  |                                                                |
| # Dashboard      |  +------------------------------------------------------------+|
| # Companies  <   |  |                                                            ||
| # Experiences    |  | [Search companies...                               ]      ||
| # Usage Logs     |  |                                                            ||
| # Point          |  | +--------------------------------------------------------+ ||
|   Adjustments    |  | | COMPANY         | ORG #     | STATUS  | EMP | BAL  | ACT|| |
| # Settings       |  | +--------------------------------------------------------+ ||
|                  |  | | TechCorp AS     | 912345678 | Active  | 12  | 1250 | ->|| |
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Nordic Well AS  | 923456789 | Active  |  8  |  830 | ->|| |
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | FoodCorp AS     | 934567890 | Active  | 15  |  420 | ->|| |
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | FitNord AS      | 945678901 | Active  |  5  |   95 | ->|| |
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Bergen Events   | 956789012 | Suspend |  3  |    0 | ->|| |
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
| Search Box | Filter companies by name or org number |
| Company Table | Company Name, Org Number, Status, Employee Count, Balance, Action arrow |
| Status Badge | Green "Active" or Red "Suspended" |
| Row Click | Navigate to Company Detail page |
| Pagination | 20 companies per page |

---

## 5. Admin - Company Detail

```
+-----------------------------------------------------------------+
|                                                                   |
|  <- Back to Companies                                             |
|                                                                   |
|  TechCorp AS                            [Active]  [Suspend]      |
|  ---------------------------------------------------------------  |
|                                                                   |
|  +---------------------------+  +---------------------------+     |
|  | Company Information       |  | Company Statistics        |     |
|  |                           |  |                           |     |
|  | Org Number  912345678     |  | Employees    12           |     |
|  | Address     Storgata 1    |  | Experiences   4           |     |
|  | City        Bergen        |  | Balance      1,250 pts    |     |
|  | Contact     Ola Nordmann  |  | Redemptions  28           |     |
|  | Email       ola@tech.no   |  | Joined       Jan 15, 2026 |     |
|  | Phone       +47 123 456   |  |                           |     |
|  +---------------------------+  +---------------------------+     |
|                                                                   |
|  +-----------------------------------------------------------+   |
|  | Employees                                    [12 total]    |   |
|  +-----------------------------------------------------------+   |
|  |                                                           |   |
|  | NAME           | EMAIL              | ROLE    | STATUS    |   |
|  | ---------------+--------------------+---------+---------- |   |
|  | Ola Nordmann   | ola@tech.no        | Owner   | Active    |   |
|  | Kari Hansen    | kari@tech.no       | Manager | Active    |   |
|  | Per Olsen      | per@tech.no        | Employee| Active    |   |
|  | Lars Berg      | lars@tech.no       | Employee| Inactive  |   |
|  +-----------------------------------------------------------+   |
|                                                                   |
+-----------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | Return to Company List |
| Company Name | Large heading with status badge |
| Status Toggle | Activate / Suspend button |
| Company Info Card | Org number, address, city, contact, email, phone |
| Stats Card | Employee count, experience count, balance, redemptions, join date |
| Employee List | Name, email, role, status for all company employees |

---

## 6. Admin - Experience List

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  EXPERIENCES                                   |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Experiences                                [45 total]        |
|    ADMIN         |  View all platform experiences                                 |
|                  |                                                                |
| # Dashboard      |  +------------------------------------------------------------+|
| # Companies      |  |                                                            ||
| # Experiences <  |  | [Search...       ]  [All Categories v]  [All Cities v]     ||
| # Usage Logs     |  |                                                            ||
| # Point          |  | +--------------------------------------------------------+ ||
|   Adjustments    |  | | EXPERIENCE   | COMPANY    |PTS|NOK    |WELFARE|STATUS  | ||
| # Settings       |  | +--------------------------------------------------------+ ||
|                  |  | | Spa Day      | Nordic AS  | 50|  1,500| [Yes] | Active | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Team Lunch   | FoodCorp   | 30|    800| [Yes] | Active | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Gym Session  | FitNord AS | 25|    600| [No]  | Active | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Cooking Class| TechCorp   | 35|  1,200| [Yes] | Active | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Movie Night  | Bergen Ev. | 20|    400| [No]  | Inactive| ||
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
| Search Box | Filter by experience title or company name |
| Category Filter | Dropdown: All, Dining, Wellness, Entertainment, etc. |
| City Filter | Dropdown: All cities |
| Experience Table | Title, Company, Points, NOK Value, Welfare Tag, Status |
| NOK Value Column | Displays "Estimated Value (NOK)" per experience (F15) |
| Welfare Tag Column | Green "Yes" badge or Gray "No" badge (F16) |
| Row Click | Navigate to Experience Detail |
| Pagination | 20 experiences per page |

---

## 7. Admin - Experience Detail

```
+-----------------------------------------------------------------+
|                                                                   |
|  <- Back to Experiences                                           |
|                                                                   |
|  Spa Day Package                                  [Active]       |
|  ---------------------------------------------------------------  |
|                                                                   |
|  +---------------------------+  +---------------------------+     |
|  | [Experience Photo]        |  | Experience Details        |     |
|  |                           |  |                           |     |
|  |                           |  | Company    Nordic Well AS |     |
|  |                           |  | Category   Wellness       |     |
|  |                           |  | City       Bergen         |     |
|  |                           |  | Points     50             |     |
|  |                           |  | NOK Value  1,500         |     |
|  |                           |  | Welfare    [Yes]         |     |
|  |                           |  | Capacity   10            |     |
|  |                           |  | Status     Active        |     |
|  +---------------------------+  +---------------------------+     |
|                                                                   |
|  +-----------------------------------------------------------+   |
|  | Description                                                |   |
|  | Full day spa experience including sauna, pool, and         |   |
|  | relaxation area. Includes lunch and refreshments.          |   |
|  +-----------------------------------------------------------+   |
|                                                                   |
|  +-----------------------------------------------------------+   |
|  | Rules                                                      |   |
|  | Must book at least 3 days in advance. Maximum 2 people     |   |
|  | per booking. Available Monday to Friday.                    |   |
|  +-----------------------------------------------------------+   |
|                                                                   |
+-----------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Back Link | Return to Experience List |
| Experience Photo | Uploaded photo display |
| Details Card | Company, Category, City, Points, NOK Value, Welfare badge, Capacity, Status |
| NOK Value | Prominently displayed estimated value in NOK (F15) |
| Welfare Badge | Green "Welfare Benefit" or Gray "Not Welfare" (F16) |
| Description | Full experience description |
| Rules | Experience rules and terms |

---

## 8. Admin - Transaction Log

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  USAGE LOGS                                    |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Usage Logs                                                   |
|    ADMIN         |  View all platform activity and export data                    |
|                  |                                                                |
| # Dashboard      |  [Transaction Log]  [Redemption Log]  [Company]  [Employee]   |
| # Companies      |                                                                |
| # Experiences    |  +------------------------------------------------------------+|
| # Usage Logs <   |  |                                                            ||
| # Point          |  | [All Companies v] [All Types v] [Date Range] [Export CSV]  ||
|   Adjustments    |  |                                                            ||
| # Settings       |  | +--------------------------------------------------------+ ||
|                  |  | | DATE    |TYPE    |FROM        |TO         |EXP  |PTS|NOK| ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 7   |Credit  |Nordic AS   |TechCorp   |Spa  |+50|1500||
|                  |  | | 14:30   |        |            |           |     |   |   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 6   |Debit   |FoodCorp    |TechCorp   |Lunch|-30| 800||
|                  |  | | 16:45   |        |            |           |     |   |   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 5   |Admin   |SwapJoys    |FitNord AS |     |+50|   | ||
|                  |  | | 10:00   |        |Admin       |           |     |   |   | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | | Apr 3   |Bonus   |System      |Bergen Ev. |     |+50|   | ||
|                  |  | | 09:00   |        |            |           |     |   |   | ||
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
| Log Tabs | Transaction Log (active), Redemption Log, Company Activity, Employee Activity |
| Company Filter | Dropdown of all companies |
| Type Filter | All, Welcome Bonus, Booking Deduction, Redemption Credit, Admin Adjustment |
| Date Range | Start / End date picker |
| Export CSV Button | Download filtered data as CSV |
| Transaction Table | Date, Type, From Company, To Company, Experience, Points, NOK Value |
| Pagination | 20 entries per page |

---

## 9. Admin - Redemption Log

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  USAGE LOGS                                    |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Usage Logs                                                   |
|    ADMIN         |  All completed experience redemptions                          |
|                  |                                                                |
|                  |  [Transaction Log]  [Redemption Log]  [Company]  [Employee]   |
| # Usage Logs <   |                                                                |
|                  |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | [All Companies v]  [Date Range]  [Export CSV]              ||
|                  |  |                                                            ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |DATE   |EMPLOYEE    |EXPERIENCE |HOST     |NOK  |WELFARE| ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 7  |Ola Nordmann|Spa Day    |Nordic AS|1,500| [Yes] | ||
|                  |  | |14:30  |TechCorp AS |           |         |     |       | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 5  |Kari Hansen |Team Lunch |FoodCorp |  800| [Yes] | ||
|                  |  | |11:00  |TechCorp AS |           |AS       |     |       | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 3  |Per Olsen   |Gym Session|FitNord  |  600| [No]  | ||
|                  |  | |16:20  |TechCorp AS |           |AS       |     |       | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  |                  [1] [2] ... [Next]                         ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Company Filter | Filter by host or requesting company |
| Date Range | Start / End date picker |
| Export CSV | Download redemption data as CSV |
| Redemption Table | Date, Employee (+ Company), Experience, Host Company, NOK Value, Welfare Tag |
| NOK Value | Estimated value at time of redemption (F15) |
| Welfare Tag | Green "Yes" or Gray "No" badge (F16) |

---

## 10. Admin - Company Activity

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  USAGE LOGS                                    |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
|                  |  [Transaction Log]  [Redemption Log]  [Company]  [Employee]   |
|                  |                                                                |
| # Usage Logs <   |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | Company: [TechCorp AS       v]  [Date Range]  [Export CSV] ||
|                  |  |                                                            ||
|                  |  | +--------------------+  +--------------------+             ||
|                  |  | | 28                  |  | 15                  |             ||
|                  |  | | Bookings Made       |  | Bookings Received   |             ||
|                  |  | +--------------------+  +--------------------+             ||
|                  |  | +--------------------+  +--------------------+             ||
|                  |  | | 22                  |  | 1,250               |             ||
|                  |  | | Redemptions         |  | Current Balance     |             ||
|                  |  | +--------------------+  +--------------------+             ||
|                  |  |                                                            ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |DATE   |EVENT              |DETAILS          |POINTS     | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 7  |Experience Redeemed|Spa Day Package  |+50        | ||
|                  |  | |Apr 6  |Booking Approved   |Team Lunch       |-30        | ||
|                  |  | |Apr 5  |Admin Adjustment   |Bonus credit     |+50        | ||
|                  |  | |Apr 3  |Booking Received   |Cooking Class    |Pending    | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Company Selector | Dropdown to select company |
| Date Range | Start / End date picker |
| Export CSV | Download company activity as CSV |
| Stats Cards | Bookings Made, Bookings Received, Redemptions, Current Balance |
| Activity Table | Date, Event Type, Details, Points |

---

## 11. Admin - Employee Activity

```
+----------------------------------------------------------------------------------+
| ADMIN SIDEBAR    |                  USAGE LOGS                                    |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
|                  |  [Transaction Log]  [Redemption Log]  [Company]  [Employee]   |
|                  |                                                                |
| # Usage Logs <   |  +------------------------------------------------------------+|
|                  |  |                                                            ||
|                  |  | Company: [TechCorp AS v]  Employee: [Ola Nordmann v]       ||
|                  |  | [Date Range]  [Export CSV]                                 ||
|                  |  |                                                            ||
|                  |  | Total NOK Value: 3,900   Welfare Total: 2,300              ||
|                  |  |                                                            ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |DATE   |EXPERIENCE    |HOST COMPANY |NOK   |WELFARE     | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 7  |Spa Day       |Nordic AS    |1,500 | [Yes]      | ||
|                  |  | |Apr 3  |Team Lunch    |FoodCorp AS  |  800 | [Yes]      | ||
|                  |  | |Mar 20 |Gym Session   |FitNord AS   |  600 | [No]       | ||
|                  |  | |Mar 10 |Cooking Class |TechCorp AS  |1,000 | [Yes]      | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Company Selector | Dropdown to select company |
| Employee Selector | Dropdown to select employee (loads after company selected) |
| Date Range | Start / End date picker |
| Export CSV | Download employee activity as CSV |
| Total NOK Value | Sum of all NOK values for selected employee |
| Welfare Total | Sum of NOK values where welfare = Yes |
| Activity Table | Date, Experience, Host Company, NOK Value, Welfare Tag |

---

## 12. Experience Detail - NOK Value & Welfare Display (Company User View)

```
+-----------------------------------------------------------------+
|                                                                   |
|  <- Back to Experiences                                           |
|                                                                   |
|  +---------------------------+  +---------------------------+     |
|  | [Experience Photo]        |  |                           |     |
|  |                           |  | Spa Day Package           |     |
|  |                           |  | by Nordic Wellness AS     |     |
|  |                           |  |                           |     |
|  |                           |  | Category: Wellness        |     |
|  |                           |  | City: Bergen              |     |
|  |                           |  |                           |     |
|  |                           |  | +-----+  +------------+  |     |
|  |                           |  | | 50  |  | NOK 1,500  |  |     |
|  |                           |  | | pts |  | Est. Value |  |     |
|  |                           |  | +-----+  +------------+  |     |
|  |                           |  |                           |     |
|  |                           |  | [Welfare Benefit]         |     |
|  |                           |  |                           |     |
|  |                           |  | Capacity: 10 spots        |     |
|  |                           |  |                           |     |
|  |                           |  | [Request Experience]      |     |
|  +---------------------------+  +---------------------------+     |
|                                                                   |
|  +-----------------------------------------------------------+   |
|  | Description                                                |   |
|  | Full day spa experience including sauna, pool...            |   |
|  +-----------------------------------------------------------+   |
|                                                                   |
+-----------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Points Badge | Point cost displayed prominently |
| NOK Value Badge | "NOK 1,500" with label "Est. Value" - new in M7 (F15) |
| Welfare Badge | Green "Welfare Benefit" badge - new in M7 (F16) |
| Request Button | Request Experience button (existing from M5) |

---

## 13. Company - Usage Documentation (Tax Reports)

```
+----------------------------------------------------------------------------------+
| SIDEBAR          |                  TAX REPORTS                                   |
| ---------------  | ------------------------------------------------------------- |
|                  |                                                                |
| [S] SwapJoys     |  Usage Documentation                                          |
|                  |  Employee experience usage for tax reporting                    |
|                  |                                                                |
| MAIN MENU        |  +------------------------------------------------------------+|
|                  |  |                                                            ||
| # Dashboard      |  | [All Employees v]  [All Welfare v]  [Date Range]           ||
| # Experiences    |  |                                                            ||
| # My Bookings    |  | Total Value: NOK 12,400   Welfare Total: NOK 8,200        ||
| # Points &       |  |                                                            ||
|   Balance        |  | +--------------------------------------------------------+ ||
| # Employees      |  | |DATE   |EMPLOYEE    |EXPERIENCE  |COMPANY  |NOK  |WELF.| ||
| # My Experiences |  | +--------------------------------------------------------+ ||
| # Tax Reports <  |  | |Apr 7  |Ola Nordmann|Spa Day     |Nordic AS|1,500|[Yes]| ||
| # Redeem Ticket  |  | +--------------------------------------------------------+ ||
| # Settings       |  | |Apr 5  |Kari Hansen |Team Lunch  |FoodCorp |  800|[Yes]| ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Apr 3  |Per Olsen   |Gym Session |FitNord  |  600|[No] | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Mar 28 |Ola Nordmann|Cooking Cls |TechCorp |1,200|[Yes]| ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  | |Mar 20 |Kari Hansen |Movie Night |Bergen Ev|  400|[No] | ||
|                  |  | +--------------------------------------------------------+ ||
|                  |  |                                                            ||
|                  |  |                  [1] [2] ... [Next]                         ||
|                  |  +------------------------------------------------------------+|
|                  |                                                                |
+----------------------------------------------------------------------------------+
```

### Elements

| Element | Description |
|---------|-------------|
| Employee Filter | Dropdown of company employees |
| Welfare Filter | All, Welfare Only, Non-Welfare Only |
| Date Range | Start / End date picker |
| Total Value | Sum of all NOK values for displayed records |
| Welfare Total | Sum of NOK values where welfare = Yes |
| Usage Table | Date, Employee, Experience, Host Company, NOK Value, Welfare Tag |
| Row Click | Navigate to usage detail (log entry detail) |
| Pagination | 20 entries per page |

---

## Component Specifications

### Status Badge Colors

| Status | Color | Background |
|--------|-------|------------|
| Active | Green (#16a34a) | Light green (#dcfce7) |
| Suspended | Red (#dc2626) | Light red (#fee2e2) |
| Inactive | Gray (#6b7280) | Light gray (#f3f4f6) |

### Welfare Tag Colors

| Tag | Color | Background | Icon |
|-----|-------|------------|------|
| Welfare Benefit (Yes) | Green (#16a34a) | Light green (#dcfce7) | Checkmark |
| Not Welfare (No) | Gray (#6b7280) | Light gray (#f3f4f6) | Dash |

### NOK Value Display

| Context | Format | Style |
|---------|--------|-------|
| Experience Card | "NOK 1,500" | Small badge, blue accent |
| Experience Detail | "NOK 1,500" with label "Est. Value" | Prominent badge |
| Table Column | "1,500" | Right-aligned, bold |
| Summary Total | "NOK 12,400" | Large, prominent |

### Metric Card Colors

| Card | Icon Color | Background |
|------|------------|------------|
| Total Companies | Blue (#244899) | Light blue |
| Total Employees | Green (#22c55e) | Light green |
| Active Experiences | Purple (#a855f7) | Light purple |
| Total Redemptions | Orange (#f97316) | Light orange |
| Points in Circulation | Blue (#6366f1) | Light indigo |

### Log Tab Colors

| Tab | Active State |
|-----|-------------|
| Transaction Log | Primary blue gradient |
| Redemption Log | Primary blue gradient |
| Company Activity | Primary blue gradient |
| Employee Activity | Primary blue gradient |

---

**Prepared by:** Rebing Tech  
**Project:** SwapJoys Platform MVP  
**Milestone:** 7 of 8
