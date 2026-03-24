# Railway Reservation Portal - File Labels

## Run Files
- `run_server.py` : Start this file to run the project in browser.
- `main.py` : Main Flask app entrypoint.
- `Procfile` : Railway deployment start command.

## Config Files
- `.env.example` : Sample environment variables.
- `.gitignore` : Files/folders excluded from Git.
- `requirements.txt` : Python dependencies.
- `README.md` : Setup guide and project overview.

## Report File
- `DBMS_MINI_PROJECT_REPORT_FINAL_SHAKSHI_PANDEY.docx` : Final project report.

## Application Folder
- `app/config.py` : App configuration.
- `app/main.py` : Flask app factory and app setup.
- `app/__init__.py` : Package entry for Flask app import.

## Database Layer
- `app/database/db.py` : SQLAlchemy engine, base, session setup.
- `app/database/__init__.py` : Database package exports.

## Models
- `app/models/entities.py` : All database table models.
- `app/models/__init__.py` : Model exports.

## Routes
- `app/routes/auth.py` : User login, register, profile routes.
- `app/routes/main.py` : Home page, history, PNR, ticket routes.
- `app/routes/booking.py` : Booking, payment, cancellation routes.
- `app/routes/admin.py` : Admin dashboard and CRUD routes.
- `app/routes/api.py` : JSON API endpoints.
- `app/routes/__init__.py` : Route blueprint exports.

## Services
- `app/services/booking_service.py` : Booking business logic.
- `app/services/report_service.py` : Dashboard and revenue reports.
- `app/services/seed_service.py` : Auto demo data seeding.
- `app/services/pdf_service.py` : PDF ticket generation.
- `app/services/notification_service.py` : Console notification mock.
- `app/services/__init__.py` : Service package export file.

## Utilities
- `app/utils/helpers.py` : Helper functions.
- `app/utils/security.py` : Password hashing, CSRF, admin checks.
- `app/utils/__init__.py` : Utility package export file.

## Frontend Files
- `app/static/css/styles.css` : Main website styling.
- `app/static/js/app.js` : Small frontend interactions.

## Templates
- `app/templates/base.html` : Shared base layout.
- `app/templates/search.html` : Home and train search page.
- `app/templates/login.html` : User login page.
- `app/templates/register.html` : User registration page.
- `app/templates/profile.html` : User profile page.
- `app/templates/booking_form.html` : Booking confirmation page.
- `app/templates/payment.html` : Payment page.
- `app/templates/booking_detail.html` : Booking summary page.
- `app/templates/history.html` : Booking history page.
- `app/templates/pnr_status.html` : PNR search page.
- `app/templates/error.html` : Error page.
- `app/templates/admin_login.html` : Admin login page.
- `app/templates/admin_dashboard.html` : Admin dashboard page.
- `app/templates/admin_trains.html` : Train management page.
- `app/templates/admin_stations.html` : Station management page.
- `app/templates/admin_routes.html` : Route management page.
- `app/templates/admin_bookings.html` : All bookings page.
- `app/templates/admin_reports.html` : Revenue report page.
- `app/templates/admin_data.html` : Live database records page.

## SQL Files
- `sql/schema.sql` : Database schema.
- `sql/seed.sql` : Sample SQL seed data.
