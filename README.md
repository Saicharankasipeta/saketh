# CarePlus Hospital Appointment Booking Demo

A responsive hospital appointment booking starter project using HTML, CSS, JavaScript, PHP (PDO) and MySQL.

## Features
- Responsive homepage and doctor cards
- Search doctors by name/specialty
- Appointment form with browser and server-side validation
- PHP endpoint stores/reuses patient details and creates appointment records
- Prevents a duplicate active booking for the same doctor/date/time in the basic demo
- MySQL tables for hospitals, patients, doctors and appointments

## Run locally on Windows with XAMPP
1. Install and open XAMPP.
2. Start **Apache** and **MySQL**.
3. Copy the `hospital_appointment_project` folder into `C:\xampp\htdocs\`.
4. Open `http://localhost/phpmyadmin`.
5. Select **Import**, choose `sql/database.sql`, and import it.
6. Open `http://localhost/hospital_appointment_project/`.
7. Submit a test appointment. The form should show a reference number.

If you rename the project folder, update the URL accordingly.

## Database connection
The default local configuration in `config/db.php` uses:
- Host: `127.0.0.1`
- Database: `careplus_hospital`
- User: `root`
- Password: blank (common default for local XAMPP only)

Change these values or set `DB_HOST`, `DB_NAME`, `DB_USER`, and `DB_PASS` environment variables to match your setup.

## Important limitations
This is an educational starter, not a production-ready hospital system. It does not yet include patient accounts/login, password reset, email/SMS confirmation, a doctor/admin dashboard, a full appointment-management page, or robust clinic-specific working-hour/holiday rules. Demo doctor cards are hard-coded in the HTML and should be fetched from the database for a production version.

Before public deployment, add authentication and authorization, CSRF protection, rate limiting, audit logging, HTTPS, secure secret management, privacy/consent notices, backup policies, and a robust race-safe slot reservation strategy. Avoid collecting unnecessary medical data. Do not store real patient data in this demo.
