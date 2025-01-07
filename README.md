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

Watch the demo of the system:  
<video controls width="600">
  <source src="Screen%20Recording%202025-01-07%20232402.mp4" type="video/mp4">
  Your browser does not support the video tag. [Download the video](Screen%20Recording%202025-01-07%20232402.mp4).
</video>

---

## Attached Images

Below are the images included in the original documentation:

### Home Page
![Home Page](assets/images/home_page.png)

### Login Page
![Login Page](assets/images/login_page.png)

### Return and Borrow Books Page
![Return and Borrow Books](assets/images/return_borrow_page.png)

### Add and Delete Books Page
![Add and Delete Books](assets/images/add_delete_page.png)

---

## Future Enhancements

- Implement user authentication for admin access.
- Add pagination for managing large datasets.
- Enable search functionality to filter books by title or author.
- Include an edit feature for updating book details.

---

## Conclusion

The **Books Management System** offers a simple and efficient way to manage a library’s inventory. Its integration of modern web technologies with a robust database ensures reliability and scalability, making it suitable for small-scale libraries or personal use.


