# Car Rental Portal

A PHP and MySQL web application for browsing rental cars, creating customer accounts, and requesting bookings. It also includes an admin area for managing cars, brands, bookings, and customer enquiries.

## Requirements

- PHP with the PDO MySQL extension
- Apache web server
- MySQL or MariaDB
- XAMPP, WAMP, or another local PHP/MySQL stack

## Run the project locally

1. Install and start Apache and MySQL using XAMPP.
2. Copy this project folder into XAMPP's `htdocs` directory. If the folder name remains `carrental`, it will be available at `http://localhost/carrental/`.
3. Create a MySQL database named `carrental` and import its schema and sample data.
   - A SQL export is not currently included in this project folder.
   - The database is required for both the customer and admin areas to work.
4. Set the database host, username, password, and database name in both:
   - `includes/config.php`
   - `admin/includes/config.php`
   - The default configuration uses `localhost`, database `carrental`, and MySQL user `root`; update `DB_PASS` for your local MySQL installation.
5. Make sure Apache has permission to write uploaded vehicle images to:
   - `admin/img/vehicleimages/`
6. Open `http://localhost/carrental/` in your browser.

## Where to start

- `index.php` — customer-facing home page and featured cars.
- `car-listing.php` — browse available cars.
- `search.php` and `search-carresult.php` — search cars.
- `vehical-details.php` — view a car and request a booking.
- `includes/` — shared website layout, database connection, login, and registration.
- `admin/index.php` — admin sign-in page.
- `admin/` — admin dashboard and management pages.
- `assets/` — website styles, scripts, fonts, and images.

## Database tables

The application queries tables such as `tblvehicles`, `tblbrands`, `tblusers`, `tblbooking`, `tbltestimonial`, `tblcontactusquery`, `tblsubscribers`, `tblpages`, and `admin`. Their SQL definitions must be imported before the pages are used.

## Typical workflows

**Customer:** Open the home page, browse or search for a car, view its details, create an account or sign in, and submit a booking request.

**Administrator:** Sign in through `admin/index.php` to manage vehicles and brands, review bookings, and handle customer messages.

## Notes

- The project uses PHP, PDO, and MySQL. PHP pages must be served through Apache; opening them directly as files will not run the application.
- The database connection settings are local configuration and may need to be updated for another computer.
- The project does not currently include Composer dependencies or an automated setup script.
- Use non-production credentials and secure the admin account before deploying this project publicly.
