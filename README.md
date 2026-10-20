# Apex Digital Library Management System

A complete, production-grade Digital Library Management System built for colleges and universities.

---

## Architecture & Technology Stack

- **Frontend**: Next.js (App Router), React, JavaScript (ES6+ ONLY), Redux Toolkit, React Redux, Tailwind CSS v3, Lucide React, Fetch API, Next.js Metadata API.
- **Backend**: Java 17, Spring Boot 3.x, Maven, Spring Web, Spring Security, JWT Authentication, Spring Data MongoDB, Jakarta Bean Validation, JUnit 5.
- **Database**: MongoDB & MongoDB Atlas compatible.
- **Deployment**: Vercel-ready frontend and Spring Boot jar backend.

---

## Project Directory Structure

```
digital-library/
├── app/                  # Next.js App Router pages & layouts
│   ├── admin/            # Administrator management portals
│   ├── catalog/          # Book catalog & dynamic details
│   ├── login/            # Authentication & demo quick login
│   ├── register/         # Student registration
│   ├── resources/        # Digital learning resources (ACM, IEEE, MIT OCW, Springer)
│   └── student/          # Student portal & dashboard
├── components/           # Reusable UI components (Navbar, Footer, Sidebar)
├── store/                # Redux Toolkit store and slices (auth, books, borrowings, reservations, fines, resources, notifications)
├── backend/              # Spring Boot 3.x Java backend
│   ├── src/main/java/com/digitallibrary/
│   │   ├── model/        # User, Book, Borrowing entities
│   │   ├── controller/   # REST Controllers
│   │   └── LibraryApplication.java
│   ├── src/test/java/    # JUnit 5 tests
│   ├── pom.xml           # Maven build configuration
│   └── src/main/resources/application.properties
└── README.md
```

---

## Features Included

1. **Authentication & Role-Based Access Control**:
   - Secure Student and Head Librarian/Administrator accounts.
   - Password hashing and JWT token handling.
   - Protected routes and demo seed credentials (`admin@college.edu` / `admin123` & `student@college.edu` / `student123`).

2. **Book Catalog & Inventory**:
   - Search by title, author, category, ISBN.
   - Categories: Computer Science, Electronics, Mechanical Engineering, Physics, Mathematics.
   - Available & total copy count tracking with real-time stock updates.
   - Admin inventory CRUD (Add, Edit, Delete books).

3. **Borrowing & Circulation**:
   - 14-day borrowing period.
   - Active borrowing lists, due dates, overdue status.
   - Self-service renewals (up to 2 times).
   - Librarian issue & return desk.

4. **Reservations**:
   - Queue-based reservations for checked-out books.
   - Position tracking, cancellation, and admin fulfillment.

5. **Fines & Payments**:
   - Overdue fine calculation ($2 per overdue day rate).
   - Balance tracking, student payment simulation, and admin collection ledger.

6. **Digital Learning Resources**:
   - Direct links to ACM Digital Library, IEEE Xplore, MIT OpenCourseWare, and Springer e-books.
   - Admin resource management.

7. **Notifications & Announcements**:
   - Due date reminders, reservation updates, and system-wide broadcast announcements.

8. **Dashboards & Analytics**:
   - Student overview of borrowings, reservations, fines, and notifications.
   - Administrator analytics on total books, active circulation, fine collection, and recent activity.

---

## Getting Started & Running

### Frontend (Next.js)
1. Install dependencies:
   ```bash
   npm install
   ```
2. Run development server:
   ```bash
   npm run dev
   ```
3. Open `http://localhost:3000`.

### Backend (Spring Boot)
1. Navigate to `backend/`:
   ```bash
   cd backend
   ```
2. Build and run with Maven (Java 17 required):
   ```bash
   mvn clean spring-boot:run
   ```
3. Run JUnit tests:
   ```bash
   mvn test
   ```
