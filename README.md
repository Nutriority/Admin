# Nutriority Admin Dashboard

A lightweight administrative dashboard for the Nutriority platform, built with static HTML/CSS/JS and Firebase.

## Overview

This repository contains the Nutriority admin console for managing users, workouts, meals, articles, reports, and sync operations.

## Key Features

- Admin login with Firebase Authentication and Firestore-based admin verification
- Real-time dashboard statistics for users, exercises, meals, and articles
- Interactive charts and overview analytics using Chart.js
- User account management including create, edit, soft delete, and password reset
- Exercise, meal, and article data management panels
- Sync center for reviewing and committing pending content imports
- User progress reporting with printable HTML/PDF-ready reports
- Idle session timeout and unauthorized access protection

## Main Files

- `admin_login.html` - login page for admin users
- `admin_dashboard.html` - main admin dashboard and navigation
- `admin_dashboard.js` - dashboard logic, authentication guard, stats, and chart rendering
- `admin_login.js` - login flow, admin verification, and error handling
- `admin_management.js` - user, exercise, meal, and article management utilities
- `admin_sync.js` - sync console and pending import workflows
- `admin_report.js` - user progress report generation
- `firebase_init.js` - Firebase configuration and exports
- `admin_dashboard.css` - dashboard styling
- `assets/` - logos, icons, and supporting images

## Setup

1. Open the project in a local web server environment.
   - Examples: Live Server extension, `python3 -m http.server`, or any static file server.
2. Ensure the Firebase project settings in `firebase_init.js` are correct for your environment.
3. Access `admin_login.html` in your browser.
4. Sign in with a Firebase-authenticated admin account whose UID exists in the `admins` Firestore collection.

## Notes

- The dashboard requires a browser that supports ES modules and modern JavaScript.
- Since Firebase uses module imports, the app should be served over `http://` or `https://`, not opened directly from the file system.
- Admin accounts must be authorized in Firestore to access `admin_dashboard.html`.

## License

This repository is only for Nutriority admins and staff. Unauthorized use, access, or distribution is prohibited.