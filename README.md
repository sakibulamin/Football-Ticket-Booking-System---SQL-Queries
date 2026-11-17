# ⚽ Football Ticket Booking System — SQL

A relational database project for a Football Ticket Booking System, designed using SQL. This project demonstrates database design, table relationships, data management, and SQL queries for handling football match ticket bookings.

## 📖 Project Overview

The Football Ticket Booking System is a database project that manages users, football matches, and ticket bookings.

It allows users to book tickets for upcoming football matches while maintaining booking records, ticket quantities, and payment amounts.

The project focuses on practicing SQL queries and understanding relational database concepts.


## 🔗 Database Relationships

- One User can have multiple Bookings.
- One Match can have multiple Bookings.
- Each Booking belongs to one User.
- Each Booking belongs to one Match.

## ✨ SQL Concepts Covered

- Database Creation
- Table Creation
- Primary Keys
- Foreign Keys
- INSERT Queries
- SELECT Queries
- WHERE Conditions
- UPDATE Queries
- DELETE Queries
- INNER JOIN
- LEFT JOIN
- GROUP BY
- HAVING
- ORDER BY
- Aggregate Functions
- Subqueries
- COUNT(), SUM(), AVG()
- DISTINCT
- LIMIT

## 🛠️ Technologies Used

- SQL
- MySQL
- Relational Database Management System (RDBMS)

## ⚙️ Database Setup

### 1. Create Database

```sql
CREATE DATABASE football_ticket_booking;
```

### 2. Select Database

```sql
USE football_ticket_booking;
```

### 3. Create Tables

Create the `Users`, `Matches`, and `Bookings` tables with their respective primary key and foreign key relationships.

### 4. Insert Sample Data

Insert sample users, football matches, and ticket bookings to practice SQL queries.

## 📊 Example SQL Queries

### Get All Users

```sql
SELECT * FROM Users;
```

### Get All Football Matches

```sql
SELECT * FROM Matches;
```

### Find Matches with Ticket Price Greater Than 1500

```sql
SELECT *
FROM Matches
WHERE ticket_price > 1500;
```

### Get Booking Details with User and Match Information

```sql
SELECT
    Users.name,
    Matches.home_team,
    Matches.away_team,
    Bookings.quantity,
    Bookings.total_price
FROM Bookings
JOIN Users ON Bookings.user_id = Users.id
JOIN Matches ON Bookings.match_id = Matches.id;
```

### Calculate Total Revenue

```sql
SELECT SUM(total_price) AS total_revenue
FROM Bookings;
```

### Find the Most Expensive Match

```sql
SELECT *
FROM Matches
ORDER BY ticket_price DESC
LIMIT 1;
```

## 📁 Project Structure

```text
Football-Ticket-Booking-System/
│
├── README.md
├── database.sql
└── queries.sql
```

## 🎯 Project Objectives

- Understand relational database design.
- Practice SQL queries with real-world examples.
- Learn Primary Key and Foreign Key relationships.
- Perform CRUD operations.
- Understand SQL JOIN operations.
- Generate booking and revenue reports.
- Improve SQL problem-solving skills.

## 🚀 Future Improvements

- Add match seat availability management.
- Add payment management.
- Add booking cancellation functionality.
- Introduce ticket status tracking.
- Add match-wise revenue reports.
- Implement stored procedures and database triggers.

## 👨‍💻 Author

**Sakibul Amin**

Full-Stack Developer

- **GitHub:** [github.com/sakibulamin](https://github.com/sakibulamin)
- **Portfolio:** [sakibul-amin.vercel.app](https://sakibul-amin.vercel.app)
- **LinkedIn:** [linkedin.com/in/sakibul-amin7](https://www.linkedin.com/in/sakibul-amin7)
- **Email:** info.sakibulamin@gmail.com

---
