# Book Inventory Management System

This is a simple PHP-based Book Inventory Management System that allows users to manage a list of books, including creating, reading, updating, and deleting book records. The application uses **XAMPP** (or any MySQL server) and **PHP** to interact with a MySQL database.
This is made as my MI College, Maldives, Web Development with PHP assginment.

---

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **XAMPP Server** or **MySQL Server**: This will host the database.
- **PHP**: Required to run the application.
- **Visual Studio Code (VS Code)**: For coding the project.

---

## Setting Up the Database

1. **Create the Database**:
   Open **phpMyAdmin** or any MySQL client (such as MySQL Workbench) and execute the following SQL to create the database and the required table.

   ```sql
   CREATE DATABASE book_inventory;
   USE book_inventory;

   CREATE TABLE books (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       author VARCHAR(255) NOT NULL,
       genre VARCHAR(100),
       published_year YEAR,
       quantity INT DEFAULT 0,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

   This will create a `book_inventory` database with a `books` table. The table stores information about books, such as title, author, genre, publication year, quantity, and timestamps.

---

## Database Configuration

In the project, the **`db.php`** file is used to manage the database connection.

1. Open **`db.php`** and configure the database connection by updating the following variables:

   ```php
   $host = '127.0.0.1'; // Server IP address (use 'localhost' if using XAMPP)
   $port = '3306'; // MySQL server port (default is 3306)
   $dbname = 'book_inventory'; // Name of the database
   $username = 'root'; // MySQL username (default for XAMPP is 'root')
   $password = ''; // MySQL password (default for XAMPP is an empty string)
   ```

---

## Running the Application

### 1. Install PHP and Visual Studio Code (VS Code)

- Install **PHP** on your machine if you haven’t already. You can download it from [PHP's official website](https://www.php.net/downloads.php).
  
- **VS Code** is recommended for editing and running the project. Download it from [Visual Studio Code](https://code.visualstudio.com/).

### 2. Install Extensions in VS Code

To make your development experience smoother:

- **PHP IntelliSense**: Provides auto-completion and IntelliSense for PHP code.
- **PHP Server Extension**: Allows you to serve the project directly from VS Code.

To install these:

1. Open VS Code.
2. Go to the **Extensions** tab (Ctrl+Shift+X).
3. Search for **"PHP IntelliSense"** and **"PHP Server"** and click **Install** for both.

### 3. Running the Project in VS Code

- Open your project folder in **VS Code**.
- In the **Explorer** sidebar, right-click on **`index.php`** and select **"PHP Server: Serve Project"**.
  
This will start a PHP server and you will be able to view your application by navigating to [http://localhost:3000/index.php](http://localhost:3000/index.php) in your browser.

---

## Project Overview

The Book Inventory Management System allows users to:

- **View all books** in the inventory.
- **Add new books** to the inventory.
- **Edit book details** such as title, author, genre, published year, and quantity.
- **Delete books** from the inventory.

The system interacts with a MySQL database to store and retrieve book information. The CRUD operations are handled using PHP and PDO (PHP Data Objects) to ensure secure database interactions.

---

## Troubleshooting

- **Database connection failed**: If you see an error like `Database connection failed: SQLSTATE[HY000] [2002] No such file or directory`, ensure that your MySQL server is running and the connection settings in **`db.php`** are correct.
- **Port Conflict**: If the PHP server doesn't work, check if port 3000 is already in use and try another port in your PHP Server extension settings.
- **NOTE**: If none of that works, call the developer Mohamed Humaam Athif at `+960 797-0977` or `mohamed.humaam.athif@gmail.com`

---

## Conclusion

Now you’re ready to manage your book inventory with this simple PHP-based system. You can further customize the interface, add more features, or enhance the security of the application as needed.

If you have any questions or issues, feel free to open an issue in the project’s repository at `github.com/mohamed-humaam/book_inventory`.