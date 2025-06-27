## Local Setup

Follow these steps to run the Movie Recommender on your local machine:

1. **Start Your Web & DB Servers**  
   - Open the **XAMPP Control Panel**.  
   - Click **Start** next to **Apache** and **MySQL**.

2. **Create the Database**  
   - In your browser, go to `http://localhost/phpmyadmin`.  
   - Click **New**.  
   - Enter **Database name:** `msrps_db`  
   - Select **Collation:** `utf8mb4_general_ci`  
   - Click **Create**.

3. **Import Schema & Seed Data**  
   - In phpMyAdmin, select the `msrps_db` database.  
   - Go to the **Import** tab.  
   - Click **Choose File** and select `./Project/Database/mrsps_db.sql`.  
   - Click **Go** and wait for the confirmation message.

4. **Deploy Project Files**  
   - Copy the entire project folder (e.g. `MovieRecommender`) into your XAMPP **htdocs** directory:  
     ```
     C:\xampp\htdocs\MovieRecommender
     ```
   - Ensure folder permissions allow read/write where needed.

5. **Configure Application Base URL**  
   - Open `initialize.php` in your editor.  
   - Locate the `$base_url` variable, for example:
     ```php
     // initialize.php
     $base_url = 'http://localhost:8080/MovieRecommender/';
     ```
   - Update the URL (and port) to match your local setup.

6. **Launch the App**  
   - In your browser, navigate to:  
     ```
     http://localhost:8080/MovieRecommender/
     ```
   - The **Movie Recommender** homepage should load.

---

### Troubleshooting

- **Database Connection Failed?**  
  - Verify **MySQL** is running in XAMPP.  
  - Double‑check credentials in `config.php`.

- **404 or Asset Loading Errors?**  
  - Make sure your project folder name matches the one in `$base_url`.  
  - Confirm files are under `htdocs/MovieRecommender`.

- **SQL Import Issues?**  
  - Open the `.sql` file in a text editor to check for corruption.  
  - Ensure your MySQL version is compatible with the dump.

- **Port Conflicts**  
  - If Apache won’t start on port **80** or **8080**, edit `httpd.conf` (search for `Listen 80`) or configure XAMPP to use a free port.
