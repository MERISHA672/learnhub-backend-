# learnhub-backend-# LearnHub Backend

## 1. Project Overview

LearnHub Backend is the server-side component of the LearnHub learning management platform. It handles API requests, communicates with the database, and provides services that support course learning and student interaction.

The backend works with the LearnHub frontend to support course discussions, learning progress tracking, and course announcements.

## 2. Key Features

- **REST API:** Provides endpoints for communication between the frontend and backend.
- **Course Discussions:** Supports creating and retrieving course-related discussion messages.
- **Learning Progress Tracking:** Stores and retrieves students' lesson completion records.
- **Course Announcements:** Supports publishing and retrieving course announcements, subject to the configured permissions.
- **Database Integration:** Stores application data in MySQL.
- **Input Validation:** Validates incoming data to help prevent invalid requests.
- **Error Handling:** Returns appropriate responses when requests fail.
- **Access Control:** Endpoints should enforce authentication, user ownership, and role permissions where required.

## 3. Technologies Used

- Node.js
- Express.js
- JavaScript
- MySQL
- npm
- Git and GitHub

## 4. Prerequisites

Before running the project, install:

- Node.js
- npm
- MySQL Server
- Git

## 5. Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/MERISHA672/learnhub-backend.git
```

### Step 2: Enter the Project Directory

```bash
cd learnhub-backend
```

### Step 3: Install Dependencies

```bash
npm install
```

### Step 4: Configure Environment Variables

Create a `.env` file in the backend root directory and configure it using the variable names required by the application.

Example configuration:

```env
PORT=5001
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=learnhub_db
```

**Important:** These variable names are examples. Check the existing backend configuration and source code to confirm the exact names expected by the application before running it.

Never commit the actual `.env` file, passwords, or other private credentials to GitHub. Use `.env.example` to document the required variable names with placeholder values.

### Step 5: Set Up the Database

1. Start MySQL Server.
2. Create or import the LearnHub database.
3. Run the database setup scripts supplied with the project.
4. Ensure the required tables and relationships exist.
5. Configure the backend to use the correct database credentials.

The database name used in the example configuration is `learnhub_db`. Confirm that it matches your actual database.

### Step 6: Start the Backend Server

Use the start command defined in `package.json`. For example, if the project defines a `start` script:

```bash
npm start
```

For development, if a `dev` script exists:

```bash
npm run dev
```

The backend is expected to run on port `5001` when configured as shown above.

## 6. Frontend Integration

The backend works with the LearnHub frontend repository:

https://github.com/MERISHA672/learnhub-frontend

Configure the frontend `.env` file with:

```env
VITE_API_URL=http://localhost:5001/api
VITE_UPLOADS_URL=http://localhost:5001
```

Ensure the backend is running, the database connection succeeds, and the frontend uses the correct API URL. Configure CORS appropriately for the frontend's development address.

## 7. Database Components

The project uses MySQL to persist application information.

Additional feature tables include:

- **`course_discussions`** — stores course discussion messages.
- **`lesson_progress`** — stores student lesson completion and progress information.
- **`announcements`** — stores course announcements.

The exact columns, foreign keys, and relationships should be verified against the database schema and setup scripts in the repository.

## 8. API Functionality

The backend provides API functionality for the frontend, including:

| Feature | Purpose |
|---|---|
| Course discussions | Create and retrieve discussion messages |
| Learning progress | Record and retrieve lesson completion |
| Course announcements | Publish and retrieve announcements |
| Database operations | Persist and retrieve application data |

The exact endpoint paths and HTTP methods should be confirmed from the project's route files.

## 9. Testing

Before demonstrating the application, verify the following:

- The backend starts without errors.
- The MySQL connection works.
- Valid requests save data successfully.
- Invalid or empty requests are rejected.
- Saved discussion messages remain available after refreshing the frontend.
- Learning progress persists after refreshing the frontend.
- Announcements can be retrieved and published by authorized users.
- Unauthorized users cannot access restricted operations.
- Existing login and course functionality continue to work.
- Errors are returned clearly when the database or server is unavailable.

Only mark a test as passed after verifying the behavior.

## 10. Security Considerations

- Keep database credentials in environment variables.
- Validate and sanitize incoming data.
- Enforce authentication and authorization on protected endpoints.
- Verify that users can access only the records they are permitted to access.
- Use parameterized database queries where supported.
- Avoid exposing sensitive information in error responses.
- Do not commit `.env` files or private credentials.

## 11. Version Control

Git is used to track source-code changes, while GitHub hosts the project repository. Meaningful commits document feature development, fixes, and improvements.

## 12. Future Improvements

Potential improvements include:

- Automated API tests.
- More comprehensive validation.
- Improved logging and monitoring.
- API documentation.
- Stronger security checks and authorization tests.
- Deployment to a production server.

## 13. Acknowledgement

This project builds upon the original LearnHub backend provided for the Web and Mobile Application Development assignment. The original authors are credited for their work, and additional features and modifications are documented as part of the coursework.

AI assistance was used for development guidance, troubleshooting, and documentation. All code and functionality should be reviewed and verified by the student.

## 14. Author

**Name:** Melissa [Insert Full Name]  
**Course:** Bachelor of Science in Information Technology (BSIT)  
**Institution:** Uganda Christian University  
**Project:** Web and Mobile Application Development Assignment

---

**Backend Repository:** https://github.com/MERISHA672/learnhub-backend
