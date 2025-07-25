markdown
User Registration System
This is a simple web-based User Registration System built using HTML, CSS, and PHP with MySQL as the database. It allows users to register with a username, email, and password.


 📂 Project Structure

register-system/
├── index.html       Registration form UI  
├── style.css        Form styling  
├── register.php     Backend registration logic (PHP)  
└── README.md        Project documentation

---

 🚀 Features

- Responsive user registration form  
- Passwords are securely hashed using PHP's password_hash()  
- Data stored in MySQL database  
- Simple and clean UI  
- Prevents SQL injection with prepared statements

---

 🛠️ Requirements

- PHP 7.x or above  
- MySQL Server  
- Apache (use XAMPP, WAMP, or LAMP stack)

---

 🧑‍💻 Setup Instructions

   1. Clone or Download
      
      Place this project folder (register-system) in your XAMPP htdocs directory:
      C:\xampp\htdocs\register-system\
      
      2. Start XAMPP
      - Launch XAMPP Control Panel  
      - Start Apache and MySQL
      
      3. Create MySQL Database
      1. Visit http://localhost/phpmyadmin  
      2. Create a new database called:
         form  
      3. Run the following SQL query to create the users table:
               ```sql
         CREATE TABLE users (
             id INT AUTO_INCREMENT PRIMARY KEY,
             username VARCHAR(50) NOT NULL,
             email VARCHAR(100) NOT NULL UNIQUE,
             password VARCHAR(255) NOT NULL,
             created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
         );
      
      4. Open in Browser
      Go to:
      [http://localhost/register-system/index.html](http://localhost/register-system/index.html)
      Fill the form and submit to register a user.

✅ Security Notes
* Passwords are hashed before storing in the database using password\_hash()
* All database interactions use prepared statements to prevent SQL injection
* Email input is validated server-side using filter\_var()


📦 Future Improvements
* Add login and logout functionality
* Add email verification
* Add password strength indicator
* Form input validation (JavaScript)
