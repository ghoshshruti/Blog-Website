# 🚀 How to Set Up and Run a Blog Website  

A blog website can be created using various technologies like **WordPress, HTML/CSS, JavaScript, PHP, or CMS platforms**. Here’s a general guide for setting up a self-hosted blog using HTML, CSS, JavaScript, and PHP with a database.

---

## 📌 1. Install Required Software  
Before building your blog, ensure you have the following installed:  

✅ **XAMPP (for local PHP & MySQL server)** → [Download XAMPP](https://www.apachefriends.org/index.html)  
✅ **VS Code or Sublime Text (for coding)**  
✅ **Git (for version control - optional)** → [Download Git](https://git-scm.com/)  

---

## 📌 2. Setting Up Your Local Server  
1. Open **XAMPP** and start:  
   - `Apache` (for PHP & web server)  
   - `MySQL` (for database)  
2. Open your browser and visit `http://localhost/phpmyadmin/`  
3. Create a **new database** named `blog_db`.  

---

## 📌 3. Setting Up Your Blog Project  
### 🔹 Create Project Folder  
1. Go to `C:\xampp\htdocs\` and create a new folder called **myblog**.  
2. Inside **myblog**, create the following files:  
   - `index.php` (Homepage)  
   - `style.css` (CSS for styling)  
   - `db.php` (Database connection)  
   - `admin.php` (Admin dashboard)  

---

## 📌 4. Writing Basic Code  

### 🔹 `db.php` (Database Connection)  
```php
<?php
$host = "localhost";
$user = "root";
$pass = "";
$dbname = "blog_db";
$conn = mysqli_connect($host, $user, $pass, $dbname);
if (!$conn) {
    die("Connection failed: " . mysqli_connect_error());
}
?>
