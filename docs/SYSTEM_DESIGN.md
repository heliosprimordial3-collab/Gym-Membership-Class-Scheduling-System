# System Design

## Use Case Diagram

![Use Case Diagram](./images/use-case-diagram.jpg)

### Use Case Diagram Description

The system has five main actors:

1. **Members** - End users who use gym facilities
2. **Trainers/Instructors** - Staff conducting classes
3. **Front Desk Staff** - Administrative staff managing operations
4. **Admin/Manager** - System administrators and managers
5. **Payment Gateway** - External payment processing system

#### Member Use Cases
- Register Account
- Login
- Manage Profile
- Browse Class Schedule
- Book Class
- Check Class Availability
- Cancel Booking
- Purchase Membership
- Upgrade Membership
- Renew Membership
- Make Payment
- Check-in to Gym
- Process Refund
- View Membership History

#### Trainer/Instructor Use Cases
- Login
- Assign Trainer to Class
- Mark Class Attendance
- Manage Class Schedule

#### Front Desk Staff Use Cases
- Login
- Manage Class Schedule
- Manage Members & Trainers
- Process Refund
- Pay via Cash/Manual

#### Admin/Manager Use Cases
- Login
- Manage Members
- Manage Trainers
- Manage Classes
- Generate Reports

#### External Actor
- **Payment Gateway** - Processes online payments securely

---

## Actor & Use Case Relationships

### Member Flow
```
┌─────────────┐
│   Member    │
└──────┬──────┘
       │
       ├─→ Register Account
       ├─→ Login
       ├─→ Manage Profile
       ├─→ Browse Class Schedule
       ├─→ Book Class
       ├─→ Check Class Availability
       ├─→ Cancel Booking
       ├─→ Purchase Membership
       ├─→ Upgrade Membership
       ├─→ Renew Membership
       ├─→ Make Payment
       ├─→ Check-in to Gym
       └─→ Process Refund
```

### Trainer/Instructor Flow
```
┌───────────────────┐
│ Trainer/Instructor│
└────────┬──────────┘
         │
         ├─→ Login
         ├─→ Manage Profile
         ├─→ Assign Trainer to Class
         └─→ Mark Class Attendance
```

### Front Desk Staff Flow
```
┌──────────────────┐
│ Front Desk Staff │
└────────┬─────────┘
         │
         ├─→ Login
         ├─→ Manage Class Schedule
         ├─→ Manage Members & Trainers
         ├─→ Process Refund
         └─→ Pay via Cash/Manual
```

### Admin/Manager Flow
```
┌────────────────┐
│  Admin/Manager │
└────────┬───────┘
         │
         ├─→ Login
         ├─→ Manage Members
         ├─→ Manage Trainers
         ├─→ Manage Classes
         └─→ Generate Reports
```

---

## UI/UX Wireframe

Below is the complete UI/UX wireframe for the Gym Membership & Class Scheduling System showing all user interfaces and flows.

### 1. Login Screen
**Common entry screen for all users (Members, Trainers, Front Desk, Admin)**

```
┌──────────────────────────────────────┐
│         GYM SYSTEM LOGO              │
├──────────────────────────────────────┤
│                                      │
│  Email/Username: [____________]      │
│                                      │
│  Password:       [____________]      │
│                                      │
│          [  Sign In  ]               │
│                                      │
│  Don't have an account? Register     │
└──────────────────────────────────────┘
```

---

### 2. Member Dashboard
**Main screen after a Member logs in**

```
┌─────────────────────────────────────────────────────────────┐
│  Dashboard      My Bookings    Membership    Make Payment    │
│  Browse Classes  Check-in      Manage Profile                │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  Welcome, John! Your membership is ACTIVE                     │
│                                                               │
│  ┌──────────────────────┐  ┌──────────────────────┐           │
│  │ Membership Status    │  │ Upcoming Classes     │           │
│  │ ACTIVE               │  │ 3                    │           │
│  └──────────────────────┘  └──────────────────────┘           │
│  ┌──────────────────────┐  ┌──────────────────────┐           │
│  │ My Bookings          │  │ Membership Plan      │           │
│  │ 2                    │  │ Monthly              │           │
│  └──────────────────────┘  └──────────────────────┘           │
│                                                               │
│  Upcoming Classes:                                            │
│  ┌──────┬─────────┬──────┬─────┬──────────┬─────────┐        │
│  │Class │ Trainer │ Date │Time │Available │ Action  │        │
│  ├──────┼─────────┼──────┼─────┼──────────┼─────────┤        │
│  │Yoga  │ Sarah   │11/15 │9AM  │ 11/15   │ [View]  │        │
│  ├──────┼─────────┼──────┼─────┼──────────┼─────────┤        │
│  │Gym   │ Mike    │11/16 │6PM  │ 8/20    │ [View]  │        │
│  └──────┴─────────┴──────┴─────┴──────────┴─────────┘        │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

---

### 3. Browse Class Schedule / Book Class
**Member checks availability before booking**

```
┌──────────────────────────────────────────────────────────────┐
│  Browse Class Schedule                    [Filter ▼]         │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌──────┬────────┬──────┬─────┬──────────┬──────────────────┐│
│  │Class │ Trainer│ Date │Time │Available │ Action           ││
│  ├──────┼────────┼──────┼─────┼──────────┼──────────────────┤│
│  │Yoga  │ Sarah  │11/15 │9AM  │ 11/15  │[Check] [Book]   ││
│  ├──────┼────────┼──────┼─────┼──────────┼──────────────────┤│
│  │Pilates│ Emma  │11/15 │11AM │ 5/10   │[Check] [Book]   ││
│  ├──────┼────────┼──────┼─────┼──────────┼──────────────────┤│
│  │Gym   │ Mike   │11/16 │6PM  │ 8/20   │[Check] [Book]   ││
│  ├──────┼────────┼──────┼─────┼──────────┼──────────────────┤│
│  │Zumba │ Lisa   │11/17 │7PM  │ 15/15 │[Check] [FULL]   ││
│  └──────┴────────┴──────┴─────┴──────────┴──────────────────┘│
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 4. My Bookings
**Member views confirmed bookings and can cancel**

```
┌──────────────────────────────────────────────────────────────┐
│  My Bookings                                                  │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌──────┬──────┬──────────┬─────────────────────────────────┐│
│  │Class │ Date │  Status  │ Action                          ││
│  ├──────┼──────┼──────────┼─────────────────────────────────┤│
│  │Yoga  │11/15 │Confirmed │ [Cancel Booking]                ││
│  ├──────┼──────┼──────────┼─────────────────────────────────┤│
│  │Gym   │11/16 │Confirmed │ [Cancel Booking]                ││
│  ├──────┼──────┼──────────┼─────────────────────────────────┤│
│  │Pilates│11/18│ Attended │ -                               ││
│  └──────┴──────┴──────────┴─────────────────────────────────┘│
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 5. Membership & Payment
**Purchase, renew, or upgrade membership, then make payment**

```
┌──────────────────────────────────────────────────────────────┐
│  Membership & Payment                                         │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  MEMBERSHIP OPTIONS:                                          │
│  ┌──────────────────┐ ┌──────────────────┐ ┌──────────────┐  │
│  │ Purchase Member. │ │ Renew Member.    │ │ Upgrade Plan │  │
│  │ $50/month        │ │ $50/month        │ │ $80/month    │  │
│  │                  │ │                  │ │              │  │
│  │  [Purchase]      │ │  [Renew] ✓       │ │ [Upgrade]    │  │
│  └──────────────────┘ └──────────────────┘ └──────────────┘  │
│                                                               │
│  PAYMENT OPTIONS:                                             │
│  ┌──────────────────┐ ┌──────────────────┐                    │
│  │Pay via Online    │ │Pay via Cash/     │                    │
│  │Gateway (Card)    │ │Manual Entry      │                    │
│  │                  │ │                  │                    │
│  │ [Pay Online]     │ │ [Pay Cash]       │                    │
│  └──────────────────┘ └──────────────────┘                    │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 6. Manage Profile
**Member updates personal information**

```
┌──────────────────────────────────────────────────────────────┐
│  Manage Profile                                               │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  Full Name:          [_______________________________]       │
│                                                               │
│  Email:              [_______________________________]       │
│                                                               │
│  Contact/Phone:      [_______________________________]       │
│                                                               │
│  Address:            [_______________________________]       │
│                                                               │
│                          [Save Changes]                       │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 7. Check-in to Gym
**Member logs entry to gym**

```
┌──────────────────────────────────────────────────────────────┐
│  Check-in to Gym                                              │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ℹ  Only active members can check in                         │
│                                                               │
│             ⭐ Your Status: ACTIVE ⭐                        │
│                                                               │
│                [  CHECK IN NOW  ]                            │
│                                                               │
│  Check-in History:                                            │
│  ┌────────────┬────────────┐                                 │
│  │ Date       │ Status     │                                 │
│  ├────────────┼────────────┤                                 │
│  │ 11/14 9:30 │ Checked-in │                                 │
│  ├────────────┼────────────┤                                 │
│  │ 11/13 6:15 │ Checked-in │                                 │
│  ├────────────┼────────────┤                                 │
│  │ 11/12 8:00 │ Checked-in │                                 │
│  └────────────┴────────────┘                                 │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 8. Front Desk Staff Dashboard
**Manage schedules, members/trainers, and process refunds**

```
┌──────────────────────────────────────────────────────────────┐
│ Manage Schedule    Manage Members    Process Refund           │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ADD CLASS:                                                   │
│  Class Name: [__________]  Trainer: [_____________]          │
│  Date: [__/____]           Time: [__:__]                     │
│  Room/Location: [_________________]                          │
│                             [Add Class]                       │
│                                                               │
│  CURRENT SCHEDULE:                                            │
│  ┌──────┬────────┬──────┬─────┬──────┬──────────┬─────────┐  │
│  │Class │ Trainer│ Date │Time │Total │ Booked  │ Action  │  │
│  ├──────┼────────┼──────┼─────┼──────┼──────────┼─────────┤  │
│  │Yoga  │ Sarah  │11/15 │9AM  │  15  │ 11      │[Edit]   │  │
│  ├──────┼────────┼──────┼─────┼──────┼──────────┼─────────┤  │
│  │Gym   │ Mike   │11/16 │6PM  │  20  │ 8       │[Edit]   │  │
│  └──────┴────────┴──────┴─────┴──────┴──────────┴─────────┘  │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 9. Trainer/Instructor Dashboard
**Assign trainers and mark class attendance**

```
┌──────────────────────────────────────────────────────────────┐
│ Assign Trainer     Mark Attendance                            │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ASSIGN TRAINER TO CLASS:                                     │
│  ┌──────┬─────────────┬──────┬──────────────┐                │
│  │Class │Current Train│ Date │  Action      │                │
│  ├──────┼─────────────┼──────┼──────────────┤                │
│  │Yoga  │ Sarah       │11/15 │[Reassign]    │                │
│  ├──────┼─────────────┼──────┼──────────────┤                │
│  │Gym   │ (Unassigned)│11/16 │[Assign]      │                │
│  └──────┴─────────────┴──────┴──────────────┘                │
│                                                               │
│  MARK CLASS ATTENDANCE:                                       │
│  ┌──────┬──────────────┬─────────────────┐                   │
│  │Class │Members Booked│   Action        │                   │
│  ├──────┼──────────────┼─────────────────┤                   │
│  │Yoga  │ 11/15        │[Mark Attendance]│                   │
│  ├──────┼──────────────┼─────────────────┤                   │
│  │Gym   │ 8/20         │[Mark Attendance]│                   │
│  └──────┴──────────────┴─────────────────┘                   │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

### 10. Admin/Manager Dashboard
**View system analytics and generate reports**

```
┌──────────────────────────────────────────────────────────────┐
│ Generate Reports    Use Cases / Procedures                    │
├──────────────────────────────────────────────────────────────┤
│                                                               │
│  ANALYTICS:                                                   │
│  ┌─────────────────┐ ┌─────────────────┐                     │
│  │ Total Members   │ │ Active Members  │                     │
│  │      120        │ │      105        │                     │
│  └─────────────────┘ └─────────────────┘                     │
│  ┌─────────────────┐ ┌─────────────────┐                     │
│  │ Total Bookings  │ │ Net Payments    │                     │
│  │      78         │ │   ₱85,000       │                     │
│  └─────────────────┘ └─────────────────┘                     │
│                                                               │
│  [Generate Report]  [Print Report]                            │
│                                                               │
│  Available Reports:                                           │
│  □ Member Reports                                             │
│  □ Financial Reports                                          │
│  □ Class Attendance Reports                                   │
│  □ Trainer Performance Reports                                │
│                                                               │
└──────────────────────────────────────────────────────────────┘
```

---

## UX Flow Diagram

### Flow 1: Member Registration & Login
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Register/    │────▶│ Authenticate │────▶│ Role-Based   │────▶│ Main Features│
│ Login Screen │     │ Credentials  │     │ Dashboard    │     │ Access       │
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

### Flow 2: Browse & Book Classes
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Browse Class │────▶│ Check Avail. │────▶│ Select & Book│────▶│ Confirmation │
│ Schedule     │     │ Spots        │     │ Class        │     │ & Receipt    │
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

### Flow 3: Membership Management
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Select Plan  │────▶│ Make Payment │────▶│ Confirmation │
│ (Purchase/   │     │ (Online/Cash)│     │ & Active     │
│ Renew/       │     │              │     │ Status       │
│ Upgrade)     │     │              │     │              │
└──────────────┘     └──────────────┘     └──────────────┘
```

### Flow 4: Booking Management
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ View My      │────▶│ Select & Can-│────▶│ Process      │
│ Bookings     │     │ cel Booking  │     │ Refund       │
└──────────────┘     └──────────────┘     └──────────────┘
```

### Flow 5: Class Management (Trainer)
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Assign       │────▶│ Mark Class   │────▶│ Generate     │
│ Trainer to   │     │ Attendance   │     │ Attendance   │
│ Class        │     │              │     │ Report       │
└──────────────┘     └──────────────┘     └──────────────┘
```

### Flow 6: System Administration
```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Admin        │────▶│ View System  │────▶│ Generate     │────▶│ Export/Print │
│ Dashboard    │     │ Analytics    │     │ Reports      │     │ Reports      │
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

---

## Color Scheme

- **Primary (Dark):** #172033 (Dark Blue-Gray)
- **Primary (Light):** #2563eb (Bright Blue)
- **Success:** #bbf7d0 (Light Green)
- **Danger:** #fecaca (Light Red)
- **Background:** #f8fafc (Light Gray)
- **Text:** #172033 (Dark)
- **Secondary Text:** #64748b (Gray)

---

## Key Design Principles

1. **Role-Based Navigation** - Each user role has different sidebar options
2. **Clear Call-to-Action** - Buttons are clearly labeled with actions
3. **Table-Based Data** - Lists shown in organized tables with action buttons
4. **Status Badges** - Visual indicators for membership and booking status
5. **Responsive Layout** - Two-column layout (sidebar + main content)
6. **Consistent Styling** - Uniform button styles, colors, and spacing

---

## Navigation Structure

```
├── Login Page
├── Member Dashboard
│   ├── Browse Class Schedule (Book Class)
│   ├── My Bookings (Cancel Booking)
│   ├── Membership (Purchase/Renew/Upgrade)
│   ├── Make Payment (Online/Cash)
│   ├── Check-in to Gym
│   └── Manage Profile
├── Front Desk Dashboard
│   ├── Manage Class Schedule
│   ├── Manage Members & Trainers
│   └── Process Refund
├── Trainer Dashboard
│   ├── Assign Trainer to Class
│   └── Mark Class Attendance
└── Admin/Manager Dashboard
    └── Generate Reports
```

---

## For Detailed Documentation

- [Database Schema](DATABASE.md) - See table structure and relationships
- [API Documentation](API.md) - See all endpoints and their usage
- [Setup Instructions](SETUP.md) - How to install and run the system
- [Project Structure](PROJECT_STRUCTURE.md) - Code organization guide
