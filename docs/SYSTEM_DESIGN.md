# System Design

## Use Case Diagram

![Gym Membership & Class Scheduling System Use Case Diagram](../images/use-case-diagram.png)

### Use Case Diagram Description

The system has four main actors:

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
- Assign Trainer to Class
- Mark Class Attendance
- Manage Class Schedule
- Manage Members & Trainers
- Generate Reports

#### Front Desk Staff Use Cases
- Manage Class Schedule
- Manage Members & Trainers
- Process Refund
- Pay via Cash/Manual

#### Admin/Manager Use Cases
- Manage Members
- Manage Trainers
- Manage Classes
- Manage Memberships
- Generate Reports
- View System Analytics

#### External Actor
- **Payment Gateway** - Processes online payments securely

---

## UI/UX Wireframe

Below is the complete UI/UX wireframe for the Gym Membership & Class Scheduling System showing all user interfaces and flows.

### 1. Login Screen
**Common entry screen for all users (Members, Trainers, Front Desk, Admin)**

- Logo: GYM SYSTEM
- Email/Username input field
- Password input field
- Sign In button
- Link to create new account

---

### 2. Member Dashboard
**Main screen after a Member logs in**

**Left Sidebar Navigation:**
- Dashboard (Active)
- Browse Class Schedule
- My Bookings
- Membership
- Make Payment
- Check-in to Gym
- Manage Profile

**Main Content:**
- Welcome greeting with membership status badge (ACTIVE)
- Stats Cards:
  - Membership Status: Active
  - Upcoming Classes: 3
  - My Bookings: 2
  - Membership Plan: Monthly
- Upcoming Classes Table:
  - Class name, Trainer, Date, Time, Availability (e.g., 11/15 spots)
  - Action buttons for each class

---

### 3. Browse Class Schedule / Book Class
**Member checks availability before booking**

**Screen Layout:**
- Page title: "Browse Class Schedule"
- Filter button for search/filtering
- Table with columns:
  - Class Name
  - Trainer Name
  - Date
  - Time
  - Available Spots (e.g., 11/15)
  - Action Buttons: "Check Availability" | "Book"

**Flow:** Member views class → Checks if spots available → Books class

---

### 4. My Bookings
**Member views confirmed bookings and can cancel**

**Screen Layout:**
- Page title: "My Bookings"
- Table with columns:
  - Class Name
  - Date
  - Booking Status (Confirmed/Cancelled/Attended)
  - Action Button: "Cancel Booking"

---

### 5. Membership & Payment
**Purchase, renew, or upgrade membership, then make payment**

**Section 1: Membership Options (3 Cards)**
1. **Purchase Membership** - Select a membership plan - "Purchase" button
2. **Renew Membership** - Continue current plan - "Renew" button (green)
3. **Upgrade Plan** - Change to better plan - "Upgrade" button

**Section 2: Make Payment (2 Cards)**
1. **Pay via Online Gateway** - External payment system - "Pay Online" button
2. **Pay via Cash/Manual** - Front desk records it - "Pay Cash/Manual" button (green)

---

### 6. Manage Profile
**Member updates personal information**

**Form Fields:**
- Full Name (text input)
- Email (text input)
- Contact/Phone (text input)
- Save Changes button

---

### 7. Check-in to Gym
**Member logs entry to gym**

- Info: "Only active members can check in"
- "CHECK IN NOW" button (primary)
- Check-in History Table:
  - Date column
  - Status column (Checked-in)

---

### 8. Front Desk Staff Dashboard
**Manage schedules, members/trainers, and process refunds**

**Left Sidebar Navigation:**
- Manage Class Schedule (Active)
- Manage Members & Trainers
- Process Refund

**Main Content - Manage Class Schedule:**

**Add Class Section:**
- Input fields:
  - Class Name
  - Trainer Name
  - Date
  - Time
  - Room/Location
- "Add Class" button

**Current Schedule Table:**
- Class Name
- Trainer Name
- Date
- Capacity (Total)
- Booked (Current bookings)
- Action buttons

---

### 9. Trainer/Instructor Dashboard
**Assign trainers and mark class attendance**

**Left Sidebar Navigation:**
- Assign Trainer to Class (Active)
- Mark Class Attendance

**Section 1: Assign Trainer to Class**
- Table columns:
  - Class Name
  - Current Trainer
  - Date
  - Action: "Assign Trainer" button

**Section 2: Mark Class Attendance**
- Table columns:
  - Class Name
  - Members Booked
  - Action: "Mark Attendance" button (green)

---

### 10. Admin/Manager Dashboard
**View system analytics and generate reports**

**Left Sidebar Navigation:**
- Generate Reports (Active)
- Use Cases / Procedures

**Main Content:**

**Analytics Stats (4 Cards):**
- Total Members: 120
- Active Members: 105
- Total Bookings: 78
- Net Payments: ₱85,000

**Reports Section:**
- "Generate Report" button
- "Print Report" button
- Available report types:
  - Member Reports
  - Financial Reports
  - Class Attendance Reports
  - Trainer Performance Reports

---

## UX Flow Diagram

### Flow 1: Member Registration & Login
```
Login/Register → Authenticate → Role Dashboard (Member) → Main Features
```

### Flow 2: Browse & Book Classes
```
Browse Schedule → Check Availability → Book Class → Confirmation
```

### Flow 3: Membership Management
```
Purchase/Renew/Upgrade Membership → Make Payment → Payment Confirmation
```

### Flow 4: Booking Management
```
View My Bookings → Cancel Booking → Process Refund
```

### Flow 5: Class Management (Trainer)
```
Assign Trainer to Class → Mark Attendance → Generate Attendance Report
```

### Flow 6: System Administration
```
Admin Dashboard → View Analytics → Generate Reports → Export/Print
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
