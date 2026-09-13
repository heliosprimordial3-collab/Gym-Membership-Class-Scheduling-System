# Database Schema

## Overview

This document describes the database structure for the Gym Membership & Class Scheduling System.

## Tables

### 1. Members

Stores information about gym members.

```sql
CREATE TABLE members (
  id INT PRIMARY KEY AUTO_INCREMENT,
  first_name VARCHAR(100) NOT NULL,
  last_name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  phone VARCHAR(20),
  date_of_birth DATE,
  gender ENUM('M', 'F', 'Other'),
  address TEXT,
  city VARCHAR(50),
  membership_id INT,
  join_date DATE NOT NULL,
  status ENUM('Active', 'Inactive', 'Suspended'),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  FOREIGN KEY (membership_id) REFERENCES memberships(id)
);
```

### 2. Memberships

Different membership plans/packages.

```sql
CREATE TABLE memberships (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100) NOT NULL,
  description TEXT,
  duration_months INT,
  price DECIMAL(10, 2) NOT NULL,
  features TEXT,
  class_limit INT,
  status ENUM('Active', 'Inactive'),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 3. Classes

Gym classes offered.

```sql
CREATE TABLE classes (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100) NOT NULL,
  description TEXT,
  instructor_id INT,
  max_capacity INT DEFAULT 20,
  schedule_day VARCHAR(20),
  schedule_time TIME,
  duration_minutes INT,
  room VARCHAR(50),
  status ENUM('Active', 'Cancelled'),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (instructor_id) REFERENCES instructors(id)
);
```

### 4. Instructors

Gym instructors.

```sql
CREATE TABLE instructors (
  id INT PRIMARY KEY AUTO_INCREMENT,
  first_name VARCHAR(100) NOT NULL,
  last_name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  phone VARCHAR(20),
  specialization VARCHAR(100),
  hire_date DATE,
  status ENUM('Active', 'Inactive'),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 5. Class Bookings

Member bookings for classes.

```sql
CREATE TABLE class_bookings (
  id INT PRIMARY KEY AUTO_INCREMENT,
  member_id INT NOT NULL,
  class_id INT NOT NULL,
  booking_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  status ENUM('Confirmed', 'Cancelled', 'Attended'),
  FOREIGN KEY (member_id) REFERENCES members(id),
  FOREIGN KEY (class_id) REFERENCES classes(id),
  UNIQUE KEY unique_booking (member_id, class_id)
);
```

### 6. Payments

Payment and billing records.

```sql
CREATE TABLE payments (
  id INT PRIMARY KEY AUTO_INCREMENT,
  member_id INT NOT NULL,
  amount DECIMAL(10, 2) NOT NULL,
  payment_date DATE NOT NULL,
  due_date DATE,
  method ENUM('Credit Card', 'Debit Card', 'Cash', 'Bank Transfer'),
  status ENUM('Paid', 'Pending', 'Overdue'),
  description TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (member_id) REFERENCES members(id)
);
```

## Relationships

```
Members (1) ──── (M) Memberships
Members (1) ──── (M) Class_Bookings ──── (M) Classes
Classes (M) ──── (1) Instructors
Members (1) ──── (M) Payments
```

## Key Constraints

- Each member can have one membership
- Each member can book multiple classes
- Each class can have multiple bookings
- Each class is taught by one instructor
- Instructors can teach multiple classes
- Payment records are linked to members

## Indexes (for performance)

```sql
CREATE INDEX idx_member_email ON members(email);
CREATE INDEX idx_member_status ON members(status);
CREATE INDEX idx_class_instructor ON classes(instructor_id);
CREATE INDEX idx_booking_member ON class_bookings(member_id);
CREATE INDEX idx_payment_member ON payments(member_id);
```

## Sample Queries

### Get active members
```sql
SELECT * FROM members WHERE status = 'Active';
```

### Get classes for a specific day
```sql
SELECT * FROM classes WHERE schedule_day = 'Monday' AND status = 'Active';
```

### Get member's booked classes
```sql
SELECT c.* FROM classes c
JOIN class_bookings cb ON c.id = cb.class_id
WHERE cb.member_id = ? AND cb.status = 'Confirmed';
```

### Get payment status for a member
```sql
SELECT * FROM payments WHERE member_id = ? ORDER BY payment_date DESC;
```

## Notes

- Dates are stored in standard format (YYYY-MM-DD)
- Timestamps include creation and update times
- Status fields use ENUM for data integrity
- Foreign keys enforce referential integrity
- Unique constraints prevent duplicate entries where needed
