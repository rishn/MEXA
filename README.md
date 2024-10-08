# MEXA

<p align="center">
  <img src="https://github.com/rishn/MEXA/blob/main/assets/MEXA.png?raw=true" alt="MEXA" />
</p>

***[MEXA](https://mexa.onrender.com/)*** is a full-stack web application designed to assist in conducting offline examinations while digitizing other educational tasks. The two primary goals of MEXA are:
1. **Reduce paper wastage** by digitizing notes, course materials, and assessments.
2. **Improve examination standards** by promoting advanced critical thinking concepts over rote learning methods.

Originally developed as a React front-end application with TypeScript, MEXA has been extended with a robust backend built using *Express.js* and *Redux* (for state management) with *MongoDB* for storing data.

[Explore the app here!](https://mexa.onrender.com/)

<p align="center">
  <img src="https://github.com/rishn/MEXA/blob/main/screenshots/dashboard.png?raw=true" alt="MEXA" />
</p>

## Demos

https://github.com/user-attachments/assets/be622d71-6450-43b5-8bd4-fd6cac17ac9d

https://github.com/user-attachments/assets/641260a0-f602-455d-8655-155aec530ba5

https://github.com/user-attachments/assets/7d873347-33de-4934-8c92-09d53a6e88d7

## Features

- **Login Form**: Secure authentication using *JSON Web Token (JWT)*.
- **Dashboard**: Overview of activities, tests, and announcements.
- **Profile Page**: View profile details, including the option to *change passwords*.
- **Examinations**: 
  - Students can take tests and view exam schedules.
  - Faculty members can invigilate exams.
  - Admins can add, edit, or delete exams.
- **Courses**: 
  - Browse and enroll in courses.
  - Students can add notes.
  - Faculty can update course materials and the number of modules taught.
- **Settings**: Customize the application theme and other preferences.

## Backend Integration

MEXA utilizes **Express.js** for its backend, **MongoDB** for data storage, and **Redux** for managing state and API calls. The backend handles user management, courses, classes, exams, and notes. Five main schemas power the system:

1. **User**: Stores user details, roles (student, faculty, admin), and credentials.
2. **Course**: Stores independent course data.
3. **Class**: Manages class-related information tied to users and courses.
4. **Exam**: Manages exam schedules, seating arrangements, and test details.
5. **Note**: Allows students to upload notes (including PDF materials).

### Key Backend Features:
- **Authentication**: JWT secures the application and user authentication.
- **Menu Locking**: During tests, the `state.disablemenu` feature locks navigation menu items and disables **breadcrumbs** to prevent students from navigating away from the test environment.
- **Navigation Blocking**: The `navigationBlock` feature ensures routing is blocked during tests, ensuring the integrity of the examination process.
- **Async Error Handling**: Middleware is in place for efficient error management in asynchronous operations.

## User Roles & Permissions

There are three user roles in MEXA, each with distinct access rights:

- **Students**:
  - Access profile, courses, and exams.
  - Can take tests, view exam schedules, and add course-related notes.
  - Can change passwords and themes.
  
- **Faculty**:
  - Access profile, courses, and exams.
  - Can update course materials, manage the number of modules taught, and invigilate exams.
  - Can change passwords and themes.

- **Admins**:
  - Full access to users, courses, classes, and exams.
  - Can add, edit, or delete users, courses, exams, and notes.
  - Can change passwords and themes.

## Frontend Tech Stack

- **React**: For building user interfaces.
- **TypeScript**: Ensures type safety and improves the development experience.
- **Redux**: Handles global state and API interactions.
- **React Router**: Enables navigation between pages like login, courses, exams, and profiles.
- **CSS**: Provides styling for the application, focusing on responsiveness and a clean user interface.

### Recent Front-End Updates:
- **Context and Hooks**: Improved handling of login persistence, prefetching, and title management.
- **Dynamic Breadcrumbs**: Automatically updated based on user role and navigation.
- **Enhanced UI/UX**: Responsive design adjustments for better cross-device compatibility.

