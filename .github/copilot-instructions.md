# Copilot Instructions for EduAuth Codebase

## Project Overview
- **EduAuth** is a PHP-based web application for educational institution management, with separate modules for admin and student users.
- The main code is in the `eduauth/` directory, with parallel structure for `student/` and shared `includes/` and `assets/`.
- Data is stored in a MySQL database, with schema in `database/eduauth.sql`.

## Key Directories & Files
- `eduauth/` — Admin-facing PHP pages (e.g., `dashboard.php`, `manage-students.php`).
- `eduauth/student/` — Student-facing PHP pages, mirroring admin structure.
- `eduauth/includes/` — Shared PHP includes: `dbconnection.php`, `header.php`, `footer.php`, `sidebar.php`.
- `eduauth/assets/` — Static assets: CSS, JS, images, SCSS, and vendor libraries.
- `credentials/username and password.txt` — Likely contains default or test credentials (do not expose in code or logs).
- `database/eduauth.sql` — MySQL schema and seed data.

## Architecture & Patterns
- **Separation of Concerns:** Admin and student modules are separated by directory, but share common includes and assets.
- **PHP Includes:** Use `include`/`require` for headers, footers, sidebars, and DB connection. Example:
  ```php
  include('includes/header.php');
  include('includes/dbconnection.php');
  ```
- **Database Access:** All DB operations go through `includes/dbconnection.php`.
- **Static Assets:** All CSS/JS/images are under `assets/` and referenced with relative paths from PHP files.
- **No Framework:** This is a custom PHP project, not using Laravel, Symfony, or other frameworks.

## Developer Workflows
- **Local Setup:**
  - Import `database/eduauth.sql` into MySQL.
  - Configure DB credentials in `includes/dbconnection.php`.
  - Serve `eduauth/` via local PHP server or Apache (e.g., `php -S localhost:8000 -t eduauth`).
- **No Automated Build/Test:**
  - No build scripts or test automation detected. Manual testing via browser is expected.
- **Static Assets:**
  - SCSS files are present but may not be auto-compiled. If editing SCSS, compile to CSS manually if needed.

## Project-Specific Conventions
- **File Naming:**
  - PHP files use kebab-case (e.g., `add-class.php`).
  - Includes are always in `includes/`.
- **Duplication:**
  - Many files are duplicated between `eduauth/` and `eduauth/student/` for role separation.
- **Security:**
  - Credentials are stored in plaintext for development; do not commit real credentials.

## Integration Points
- **Database:** MySQL, schema in `database/eduauth.sql`.
- **No External APIs** detected.

## Examples
- To add a new admin page: copy an existing PHP file in `eduauth/`, update logic, and include shared headers/footers.
- To add a new student page: do the same in `eduauth/student/`.

---

**Update this file if you add new workflows, conventions, or integration points.**
