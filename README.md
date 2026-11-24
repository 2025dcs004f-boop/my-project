# Transport Management System (Yii 2)

USJM Diploma in Computer Science – Mid-Semester One 2026/2027. Framework: **Yii 2 (basic app)**.

## Requirements
PHP 7.4+ (8.x fine) with `pdo_mysql`, `mbstring`, `intl` (recommended), Composer, MySQL/MariaDB (XAMPP is fine).

## Setup
1. Extract the folder, open a terminal inside it, then install Yii2:
   ```
   composer install
   ```
2. Create the database – choose ONE:
   - **Option A (sample data):** import `database/tms_db.sql` in phpMyAdmin (or `mysql -u root < database/tms_db.sql`).
   - **Option B (migration):** create an empty database `tms_db`, then run `php yii migrate` (creates tables + admin only).
3. Check database login in `config/db.php` (default: `root`, empty password, db `tms_db`).
4. Start the server:
   ```
   php yii serve --docroot=web
   ```
   then open http://localhost:8080/index.php

   (With XAMPP you can instead copy the folder into `htdocs` and open `http://localhost/tms/web/index.php`.)

## Login accounts
| Role | Username | Password |
|---|---|---|
| Admin | `admin` | `password` (SQL import) or `Admin@123` (migration) |
| Passenger | `passenger1` | `password` (SQL import only) |

Passengers can also register themselves on the Register page. Change default passwords after first login.

## Main pages
`?r=site/index` Home · `site/login` · `site/register` · `site/dashboard` · `site/trips` · `payment/pay&trip_id=1` · `payment/my` · admin: `vehicle`, `driver`, `route`, `trip`, `payment`, `report/monthly`.

## Structure
`config/` settings · `controllers/` · `models/` · `views/` · `migrations/` · `database/tms_db.sql` · `docs/` documentation & ERD · `web/` public root.

Documentation for the exam (Questions 1–5) is in `docs/PROJECT_DOCUMENTATION.docx` (also `.md`).
