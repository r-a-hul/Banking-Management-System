# Java Banking System Console Application

A simple Java-based console application that simulates core banking functionalities such as user registration, login, account management, and secure transactions. This project uses JDBC for database operations with a MySQL backend.

---

## Project Structure

This project contains the following classes:

- `Main.java` – Entry point and application flow controller
- `User.java` – Handles user registration and login
- `Accounts.java` – Manages account creation and retrieval
- `AccountManager.java` – Handles credit, debit, balance check, and money transfers

---

## Features

- User registration and login with email/password
- Create a new bank account
- Debit and credit money
- Check account balance securely
- Transfer money between accounts
- Secure transactions using a security PIN
- Uses JDBC for MySQL database interaction

---

## Tech Stack

- **Java**
- **JDBC**
- **MySQL**

---

# Sample Flow

*** WELCOME TO BANKING SYSTEM ***

1. Register
2. Login
3. Exit
Enter your choice: 1

  Full Name: Rahul Singh
  Email: rahul@example.com
  Password: ********

  Registration Successful!

...

  Enter your choice: 2
  Email: rahul@example.com
  Password: ********

User Logged In!

1. Debit Money
2. Credit Money
3. Transfer Money
4. Check Balance
5. Log Out
Enter your choice: 4

Security Pin: ****
Balance: Rs. 5000


---


## Database Setup

Ensure you have MySQL installed and create a database with the following tables:

```sql
CREATE DATABASE banking_system;

USE banking_system;

CREATE TABLE Users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(100)
);

CREATE TABLE Accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100),
    balance DOUBLE,
    security_pin VARCHAR(10)
); 
