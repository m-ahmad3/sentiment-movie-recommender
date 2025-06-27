Step-by-Step Guide to Run the Project Locally
1. Start XAMPP
Launch the XAMPP control panel.
Start Apache and MySQL services.
2. Create Database
Open phpMyAdmin via http://localhost/phpmyadmin.
Create a new database named msrps_db (Collation: utf8mb4_general_ci).
3. Import Database
Navigate to the Import tab in phpMyAdmin.
Upload the mrsps_db.sql file located in ./Project/Database.
Click Go to import tables.
4. Set Up Project Folder
Copy the entire project folder (e.g., MovieRecommender) into the htdocs directory
(usually C:\xampp\htdocs).
5. Configure Base URL
Open initialize.php in a code editor.Locate the base_url variable.
Replace it with your local server path, e.g.:
$base_url = 'http://localhost:8080/MovieRecommender/';
(Adjust port 8080 or folder name as needed)
6. Run the Project
Open your browser and navigate to:
http://localhost:8080/MovieRecommender
The Movie Recommender homepage should load.
Troubleshooting Tips
🔧 Database Connection Failed?
Ensure MySQL is running in XAMPP.
Verify database credentials in config.php.
🔧 404 Errors?
Double-check the base_url in initialize.php.
Confirm the project folder is in htdocs.
🔧 SQL Import Issues?
Ensure the .sql file is not corrupted.
Check for PHP version compatibility.
