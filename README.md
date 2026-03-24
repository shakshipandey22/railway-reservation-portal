# Railway Reservation System

A full Railway Reservation System built with Python, Flask, SQLAlchemy, MySQL, Jinja templates, and vanilla CSS/JavaScript.

## Features

- Passenger registration, login, logout, and profile management
- Secure password hashing with `bcrypt`
- Search trains between two stations by date
- Seat inventory generation by train, class, and travel date
- Booking workflow with automatic PNR generation
- Dynamic seat allocation with waitlist fallback
- Simulated payment handling for UPI, Card, and Net Banking
- Ticket cancellation with refund simulation and waitlist promotion
- PNR status check
- Booking history
- PDF ticket download
- Console-based email/notification mock
- Admin dashboard for trains, stations, routes, bookings, and revenue
- Admin database viewer (`/admin/data`) for all required tables
- API endpoints for train search, PNR lookup, and admin stats

## Project Structure

```text
app/
  database/
  models/
  routes/
  services/
  static/
  templates/
  utils/
main.py
sql/
requirements.txt
```

## Database Notes

The app uses these MySQL table names exactly:

- `train`
- `station`
- `route`
- `passenger`
- `booking`
- `seat`
- `payment`
- `admin_user`

If your `railway_db` already exists, point the app to it in `.env`. If you need a compatible schema, use [`sql/schema.sql`](C:\Users\shaks\OneDrive\Documents\New project\sql\schema.sql) and sample data from [`sql/seed.sql`](C:\Users\shaks\OneDrive\Documents\New project\sql\seed.sql).

## Setup

1. Create a virtual environment:

```powershell
python -m venv .venv
.venv\Scripts\activate
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
```

3. Create your environment file:

```powershell
Copy-Item .env.example .env
```

4. Update `.env` with your MySQL credentials.

5. Optional: create the schema and seed sample data:

```sql
SOURCE sql/schema.sql;
SOURCE sql/seed.sql;
```

6. Run the application:

```powershell
python main.py
```

7. Open the app in your browser:

```text
http://127.0.0.1:5000
```

## Default Admin Login

The app bootstraps a default admin user on startup from `.env`:

- Username: `admin`
- Password: `Admin@123`

Change both values in `.env` before using the app outside local development.

## Demo Passenger Login

Auto-seeded demo users (created when `AUTO_SEED_DATA=true`):

- Email: `demo.user@example.com` | Password: `Demo@12345`
- Email: `riya.sharma@example.com` | Password: `Demo@12345`

## API Examples

### Search trains

```text
GET /api/trains/search?source_station_id=1&destination_station_id=5&travel_date=2026-03-25
```

### Check PNR

```text
GET /api/pnr/PNR260325123456
```

### Admin stats

```text
GET /api/admin/stats
```

## Important Assumptions

- Seat inventory is generated per train and travel date.
- Waitlist promotion is handled at train-date-class level.
- Search validity depends on correctly configured `route.stop_number` values.
- The provided SQL reflects a compatible schema using the exact required table names.
