# Books Management System

## Overview

The **Books Management System** is a web-based application designed for managing library books effectively. This system allows users to view, add, and delete books in a PostgreSQL database through a user-friendly interface. Built using **Node.js**, **Express.js**, and **EJS**, it is ideal for small libraries or personal use.

## Features

1. **View All Books**  
   - Displays all books stored in the database.
   - Shows details such as:  
     - Book ID  
     - Title  
     - Author  
     - Publication Year  
     - Availability  

2. **Add New Books**  
   - Input form to add new book details:  
     - Title  
     - Author  
     - Publication Year  
     - Availability (Available/Not Available)  

3. **Delete Books**  
   - Remove books by their ID with a confirmation prompt to prevent accidental deletions.

4. **User-Friendly Interface**  
   - Clean and modern design for easy navigation.

## Technologies Used

### Frontend
- **HTML**: Webpage structure.
- **CSS**: Styling the interface.
- **EJS**: Dynamic content rendering.

### Backend
- **Node.js**: Server-side programming.
- **Express.js**: Web framework for routing and request handling.
- **Body-Parser**: Middleware for parsing form data.

### Database
- **PostgreSQL**: Relational database for storing book records.

## System Requirements
- **Node.js** (v12 or higher)
- **PostgreSQL** (v12 or higher)
- Web browser

## Database Schema

### Table: `books`

| Column            | Type          | Description                  |
|--------------------|---------------|------------------------------|
| `id`              | SERIAL        | Primary Key                  |
| `title`           | VARCHAR(255)  | Title of the book            |
| `author`          | VARCHAR(255)  | Author of the book           |
| `publication_year`| INT           | Year of publication          |
| `availability`    | BOOLEAN       | Availability status          |

### Sample SQL Query
```sql
CREATE TABLE books (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255) NOT NULL,
    publication_year INT NOT NULL,
    availability BOOLEAN NOT NULL
);
