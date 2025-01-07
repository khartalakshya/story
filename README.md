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
# Books Management System

## Installation and Setup

### Clone the Repository
```bash
git clone https://github.com/khartalakshya/story.git
cd story
```

### Install Dependencies
```bash
npm install
```

### Configure Database

1. Ensure PostgreSQL is running.
2. Update the database connection details in the backend code:
    ```javascript
    const db = new Pool({
        user: "your_username",
        host: "localhost",
        database: "your_database",
        password: "your_password",
        port: 5432,
    });
    ```

### Start the Server
```bash
node app.js
```

### Access the Application

Open your browser and navigate to:  
[http://localhost:3000/books](http://localhost:3000/books)

---

## File Structure

```
story/
├── public/            # Static files (CSS, images, etc.)
├── views/             # EJS templates
│   ├── books.ejs      # Main books page
├── app.js             # Backend server
├── package.json       # Project metadata and dependencies
```

---

## Routes

1. **`/books` (GET)**  
   - Displays all books.

2. **`/books/add` (POST)**  
   - Adds a new book to the database.

3. **`/books/delete/:id` (POST)**  
   - Deletes a book by its ID.

---

## Demo Video

[Watch or Download the Demo Video](Screen%20Recording%202025-01-07%20232402.mp4)

---

## Future Enhancements

- Implement user authentication for admin access.
- Add pagination for managing large datasets.
- Enable search functionality to filter books by title or author.
- Include an edit feature for updating book details.

---

## Conclusion

The **Books Management System** offers a simple and efficient way to manage a library’s inventory. Its integration of modern web technologies with a robust database ensures reliability and scalability, making it suitable for small-scale libraries or personal use.

